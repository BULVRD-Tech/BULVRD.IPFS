# BULVRD.IPFS
Repo for documentation related to BULVRD validated data being sent + stored on IPFS

## The Spec
BULVRD app(s) will post validated reports + data to IPFS. An example of validation includes reports with 2+ up vote confirmations. Future validations will include reports with stakes and Proof of Location validators. 

Data will be posted directly to IPFS in json format. BULVRD will run it's own IPFS node and pin all validated data. The data sets will be structured with the following values:
- type : String - Constant of report type
- id : String - Unique identifier of report object
- addy : String - Wallet address of original reporter
- geohash : String - Geohash for location of report, 12pt precision
- timestamp : Long - Millisecond timestamp of report creation
- validator : String - Constant value of how report was validated

For a working example:
`
{
"geohash" : "dqcj4s6zwzsn",
"type" : "Traffic",
"addy" : "0x123456",
"id" : "12345",
"timestamp" : 1534640601,
"validator" : "Votes"
}
`

## The Spec
BULVRD will leverage set report types, stored as constant values. Here we will outline the current supported values. These values will expand overtime as community needs arise.

- Police
- Closure
- Traffic
- Hazard
- Construction
- Speed Cam
- Red Light Cam
- Accident
- Speed Trap
- Wildlife
- Weather Alert
- Police Checkpoint
- Pothole
- Speed Bump
