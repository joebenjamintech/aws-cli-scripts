## AWS Logs (logs)

A script created to get the logs using the aws cli.

### Options

* `-m`: min time - all events must be greater than or equal to min time  
* `-M`: max time - all events must be less than or equal to max time  
* `-t`: menu type - supports fzf and dmenu --- if not fzf, then defaults to dmenu, else fzf  
* `-p`: stream prefix - used to search the streams by a stream prefix of the name  
* `-n`: next token - pages to the next set of streams from prev call, will use group from prev call  
* `-b`: next backward token - pages to the next event going backwards, will use group and stream from prev call  
* `-f`: next forward token - pages to the next event going forwards, will use group and stream from prev call  
* `-g`: group - will use group from prev call  
* `-s`: stream - will use group and stream from prev call  

### Vars file

The vars file will be saved in the directory the script is ran in.  This file is use to hold values from other calls.  Think of it as a settings file.

### Date Time

The script uses the local time which is sent to AWS and that gets translated into UTC time and also comes back in UTC time.
Pass all of your date time params in your local time.

### Sample calls

* `aws_logs`
* `aws_logs -m "2023/03/15 05:22" -M "2023/03/16 12:00"`
* `aws_logs -s -t dmenu`

