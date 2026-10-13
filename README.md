# minimal-reproduction-template

46998 

## Current behavior

Dispate having the `minimumReleaseAge` globally at `7 days`, there are MRs created with updates younger then 7 days. 

It seems like the `security:minimumReleaseAgeNpm` preset is not respecting the maximum of the `minimumReleaseAge` and `.npmrc`. 

```
            {
                "internalChecksFilter": "strict",
                "matchDatasources": [
                    "npm"
                ],
                "minimumReleaseAge": "3 days"
            },
```

Running self-hosted on self-hosted GitLab.

![alt text](data/image.png)

## Expected behavior

Only add packages which are at minimumal `7 days` old, not younger. 

## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/46998