## terms
`ro`: remember object, a single entity that is to be remembered

## Features
- user to provide their data (source of truth)
  - each data entry should have enough ros
  - one type of data should share the same ro types
- quiz can be generated with the data
  - user to provide the scope for the quiz
  - user can customize choice count / quiz count
- quiz statistics/storage
  - correct rate/count of each ro

## Tech choices

### Frontend
react native:
- popular in and out
- js/ts used at work as well

### Storage
local file db?

## Components breakup

### data definition
Define data type and data.
Data type is like class, data is like instance.

### quiz generation
Given data scope, ro type, quiz size => generate quiz

### quiz statistics
Together with quiz generation, store the quiz result statistics while user is taking the quiz.

## Tasks

0. investigate tech choices
week =======
- react native with simple quiz
- test on mobile
week =======
- local file db:
  - realm (object based): chosen, supporting offline, NoSQL, depending on local file and can be synced with cloud
  - Redux Offline
  - https://stackoverflow.com/questions/41896719/backup-realm-to-icloud-drive
  - https://medium.com/code-well/choosing-the-right-database-for-your-react-native-app-137f4893b182
  - https://www.powersync.com/blog/react-native-local-database-options
  - https://www.mindinventory.com/blog/top-react-native-databases/
- where to upload the local file db?
  - use with cloud?

data/service api layer only
week =======
1. data definition
    - define data type
    - define data for testing
week =======
2. quiz generation
week =======
3. save quiz statistics

UI integrations
week =======
4. display quiz statistics