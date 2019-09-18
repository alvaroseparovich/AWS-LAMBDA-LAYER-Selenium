# AWS-LAMBDA-LAYER-Selenium
This is a Selenium Layer for AWS Lambda, it is ready to use.

![alt text](https://a.fsdn.com/allura/p/idlex/icon?1452779543?&w=90)
Tested on python3.6

----

To start it you need only to know how to begin.
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

------

In the same archive you have a file called python/**lambda_function.py**  if you dont wanna create a Lambda Layer you can use the same archive to run your function, and this file you will find a ready to use function, ready to be uploaded unto S3 and to be trigged. Change what you want as you need.
