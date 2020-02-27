
Steps for Creating custom aws lambda
====================================

1) Create the virtual env, activate and install required packages
    
    python3 -m venv env
    source env/bin/activate
    
    pip install pandas==0.23.4
    
    pip install boto3

    # install required packages in the env

2) create lambda_function.py with required logic and copy over this file into site-packages folder of the env

3) zip all the files present inside the site-packages as below
    package.zip
      |
      |- pandas module folder
      |- boto3 module folder
      |- some other folders
      |- lambda_function.py
      |- some other files

4) Create lambda function with required permissions

5) Once can upload the zip file directly in lambda and zip file size should must be < 250MB
      or
   Once can upload the zip file in S3 and give the path in lambda
   
   
