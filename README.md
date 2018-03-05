# User Onboarding CLI Tool
A python script to transform csv/json/yaml/arguments into json and posts to create VictorOps accounts in bulk.

## Usage
```sh
# Manually add one user
./onboard_victorops_user create --apiId asd --apiKey asd --username foo --email foo@bar.gov --firstName foo --lastName bar --phone 1111111111 --orgRole member --teams team1:member,team2:member

# Upload CSV
./onboard_victorops_user csv -f accounts-example.csv --apiId abc --apiKey 123

# Upload JSON
./onboard_victorops_user json -f accounts-example.json --apiId abc --apiKey 123

# Upload YAML
./onboard_victorops_user yaml -f accounts-example.yaml --apiId abc --apiKey 123
```

## Roles
In VictorOps, the following roles are supported when adding members
* Team
    * team_admin
    * member
* Organization
    * admin
    * team_admin
    * member

## Formats
Examples of the expected JSON, YAML, and CSV formats are in the respective `accounts-example` files in this repo.

Since the fields of orgAdmin and teams are optional, the fields can be left blank in the file.
