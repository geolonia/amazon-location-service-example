# SANDBOX Amazon Location Service

## Demo

[https://geolonia.github.io/sandbox-amazon-location-service/](https://geolonia.github.io/sandbox-amazon-location-service/)

## Dependencies

- Amazon Location Serice
    - A map named `explore.map`
- Amazon Cognito Identity Pool
    - A pool with the role described below:
    ```json
    {
    "Version": "2012-10-17",
        "Statement": [
            {
                "Sid": "MapsReadOnly",
                "Effect": "Allow",
                "Action": [
                    "geo:GetMapStyleDescriptor",
                    "geo:GetMapGlyphs",
                    "geo:GetMapSprites",
                    "geo:GetMapTile"
                ],
                "Resource": "arn:aws:geo:ap-northeast-1:{AWS Account ID}:map/explore.map"
            }
        ]
    }
    ```
