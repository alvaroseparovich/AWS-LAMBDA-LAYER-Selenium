# AWS-LAMBDA-LAYER-Selenium
This is a Selenium Layer for AWS Lambda, it is ready to use.

To start it you need only to know how to start it.
here is a quick start

Lambda function
----------------
here is an example of function:
```
import starter as st

def lambda_handler(event, context):
    driver = st.start_drive()
    driver.get('https://www.google.com.br')
    page_data = driver.page_source
    driver.close()
    return page_data
```
Do not forget to change your Lambda Function's Memory to at leats 384 mb, and the time out at least 30 sec
