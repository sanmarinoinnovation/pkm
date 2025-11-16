Next steps:

Your DSC’s has to be uploaded to the gateway
At least one DSC has to be deleted again
The trustlist should be downloaded from the gateway

Please find below steps to check the connectivity with the Trust Network Gateway.

TNG-WHO Endpoints:
- UAT:      `https://tng-uat.who.int`
- DEV:     `https://tng-dev.who.int`

## Upload CMS Package:

`curl -v -X POST -H "Content-Type: application/cms" --cert TLS.pem --key TLS.key --data @cms.b64 << Replace with Env Specific Endpoint>>/signerCertificate`

UAT:
`curl -v -X POST -H "Content-Type: application/cms" --cert TLS.pem --key TLS.key --data @cms.b64 https://tng-uat.who.int/signerCertificate`

DEV:
`curl -v -X POST -H "Content-Type: application/cms" --cert TLS.pem --key TLS.key --data @cms.b64 https://tng-dev.who.int/signerCertificate`

## Delete CMS Package:

`curl -v -X DELETE -H "Content-Type: application/cms" --cert TLS.pem --key TLS.key --data @cms.b64 << Replace with Env Specific Endpoint>>/signerCertificate`

Get trustlist : (Please replace actual endpoint accordingly)
`curl -v Endpoint/trustList --cert TLS.pem --key TLS.key`

Please keep in mind that
The standard onboarding process has to be implemented to ensure that your country is able to renew the certificates.

For details, see
https://github.com/WorldHealthOrganization/tng-participant-template
and
https://worldhealthorganization.github.io/smart-trust/concepts_onboarding.html