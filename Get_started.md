## Get credentials
* Log into AWS portal where you should see your account listed. 
* Link to "Access keys" will give you credentials to use AWS outside of a browser.

## Configure AWS CLI
* Log into one of the rhino machines via ssh.
* Load the awscli module (```ml awscli```)
* Run ```aws configure sso```
* SSO session name => any string
* SSO start URL => enter the SSO start URL shown in your browser
* SSO region => enter us-west-2
* SSO registration scopes => press Enter

* You will now see a URL and code displayed. Copy paste the URL into your browser. 
* Click Allow Access.

* Choose the AWS account (if you have multiple accounts)
* CLI default client Region => press Enter
* CLI default output format => press Enter
* CLI profile name => 
* ``` To use this profile, specify the profile name using --profile, as shown:
* aws s3 ls --profile default ```
