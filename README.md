# CTFd-S3-plugin
Plugin that converts CTFd file uploads and deletions to Amazon S3 calls.

AWS S3 support has been integrated into CTFd as of version 2.0. 

## Installation

1. To install clone this repository to the [CTFd/plugins](https://github.com/isislab/CTFd/tree/master/CTFd/plugins) folder.
2. Install the requirements specified in the [requirements.txt](https://github.com/CTFd/CTFd-S3-plugin/blob/master/requirements.txt) file. 
3. Edit [CTFd/config.py](https://github.com/isislab/CTFd/blob/master/CTFd/config.py) and add the following entries:
  * S3_ACCESS_KEY_ID
  * S3_SECRET_ACCESS_KEY
  * S3_BUCKET
  * S3_ENDPOINT_URL (optional)

`S3_ACCESS_KEY_ID` is your AWS Access Key. If you do not provide this, the plugin will try to use an IAM role or credentials file.

`S3_SECRET_ACCESS_KEY` is your AWS Secret Key. If you do not provide this, the plugin will try to use an IAM role or credentials file.

`S3_BUCKET` is the name of your Amazon S3 bucket. 

`S3_ENDPOINT_URL` is the endpoint url of your Amazon S3 bucket. 

## Note

This plugin will not yet backfill any files you've uploaded. If you install the plugin after you've uploaded files, you will need to upload your current challenge files to S3. 
