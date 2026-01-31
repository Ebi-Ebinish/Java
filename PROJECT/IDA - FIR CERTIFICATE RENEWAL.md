
When the Public key certificate expired means we need to renewal that use these step:

https://apps.pdccl.philsys.gov.ph/v1/authmanager/swagger-ui.html#/authmanager

above the URL is AUTH manager go to the 

https://apps.pdccl.philsys.gov.ph/idauthentication/v1/internal/swagger-ui.html#/keymanager/generateSymmetricKeyUsingPOST  

The above link is swagger URL in that go to Get-Certificate API -
https://apps.pdccl.philsys.gov.ph/idauthentication/v1/internal/getCertificate?applicationId=IDA&referenceId=IDA-FIR

That certificate will check the certificate data whether the certificate has expired or not if expires means it will give the response to expires extended certificate
