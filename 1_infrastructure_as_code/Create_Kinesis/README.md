# Creating a data stream with Kinesis


Here we will create a Data Stream, we will deploy:
* Kinesis Stream
* Kinesis Delivery Stream
* Kinesis Firehose
* Log Group
* Log Stream
* Bucket
* IAM Role
* IAM Policy

Deploy:
1. Navigate to the Cloudformation page on your AWS console
1. Click create stack -> with new resources
1. Upload the YAML file and follow the instructions to deploy


Use:
1. We recommend creating a virtual-env
    ``
    pip install virtualenv
    my-project cd /
    virtualenv venv
    source venv / bin / activate
    # venv \ Scripts \ activate.bat on Windows
    ``
1. Install the requirements.txt dependencies
    ``
    pip install -r requirements.txt
    ``
1. Add your AWS credentials to the environment variables
    1. Create a profile in `~ / .aws / config`
        ``
        [profile my_aws_profile]
        aws_access_key_id = AK ...
        aws_secret_access_key = sl ...
        region = us-east-1
        ``
    1. Add to the environment: ʻexport AWS_PROFILE = my_aws_profile` or add to your `.bashrc` if you want
    persist the variable to other sessions
    1. Run the Python script `put_records_in_kinesis.py`
    
Your event stream is now sent to Kinesis, and persisted from there on S3.