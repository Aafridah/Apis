
# Introduction

Gets SMS campaign details.

# Overview

URL : https://{domain}/api/GetSmsCampaignDetails  
Method : Post/Get  
ContentType : json  
Parameters :  
\=======================

| key | Value |
| --- | --- |
| api_key | "" |
| api_password | "" |
| date | date(optional) |
| job_id | job_id(optional) |
| dlr_status | dlr_status(optional) |

# Response:

if(job_id not supplied)

``` json
{
    "Success": true,
    "ErrorCode": 1000,
    "Remarks": "Ok",
    "CampaignDetail": [
        {
            "JobId": 11,
            "JobName": "abc",
            "JobDateTime": "2023-09-06T16:53:27",
            "TotalSms": 22,
            "DlrStatus": {
                "None": null,
                "Enroute": null,
                "Delivered": null,
                "Expired": null,
                "Deleted": null,
                "Undeliverable": null,
                "Accepted": null,
                "Unknown": null,
                "Rejected": null,
                "Pending": 22,
                "Submitted": null,
                "DND": null,
                "Failed": null,
                "Acknowledged": null
            }
        },
        {
            "JobId": 12,
            "JobName": "abc",
            "JobDateTime": "2023-09-06T16:56:59",
            "TotalSms": 22,
            "DlrStatus": {
                "None": null,
                "Enroute": null,
                "Delivered": null,
                "Expired": null,
                "Deleted": null,
                "Undeliverable": null,
                "Accepted": null,
                "Unknown": null,
                "Rejected": null,
                "Pending": 22,
                "Submitted": null,
                "DND": null,
                "Failed": null,
                "Acknowledged": null
            }
        },
        {
            "JobId": 13,
            "JobName": "abc",
            "JobDateTime": "2023-09-06T17:02:15",
            "TotalSms": 22
            "DlrStatus": {
                "None": null,
                "Enroute": null,
                "Delivered": null,
                "Expired": null,
                "Deleted": null,
                "Undeliverable": null,
                "Accepted": null,
                "Unknown": null,
                "Rejected": null,
                "Pending": 22,
                "Submitted": null,
                "DND": null,
                "Failed": null,
                "Acknowledged": null
            }
        }
    ]
}

 ```

(if job_id supplied) :

``` json
{
    "Success": true,
    "ErrorCode": 1000,
    "JobId": 5,
    "JobName": null,
    "JobDateTime": "2023-09-06T15:58:13",
    "TotalSms": 0,
    "CampaignDetail": [
        {
            "JobDetailId": 0,
            "PhoneNumber": null,
            "DlrStatus": null
        }
    ],
    "Remarks": "OK"
}

 ```

# Authentication

api_key : Customer's api_key  
api_password : Customer's api_password

# Error Codes

``` csharp
enum ErrorCodes
        {
            NoError = 1000,
            DateNotSpecified = 1001,
            ApiKeyNotSpecified = 1003,
            ApiPasswordNotSpecified = 1004,
            InvalidApiKey = 1005,
            InvalidApiPassword = 1006,
            ApiIsNotEnabledForThisAccount = 1007,
            ParametersNotSupplied = 1008,
            JobIdNotSpecified = 1009,
            NoJobDataFound = 1010,
            InvalidDlrStatus = 1011
        }

 ```

# Rate limit

No
