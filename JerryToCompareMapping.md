# Jerry to Compare mapping

## Carrier names

```javascript
{
    "21stCentury": "TwentyFirstCentury",
    "AAA": "AAA",
    "Allstate": "Allstate",
    "AmericanFamilyInsurance": "AmericanFamily",
    "BristolWest": "BristolWest",
    "ElephantAutoInsurance": "Elephant",
    "EncompassInsuranceCompany": "Encompass",
    "ErieInsurance": "Erie",
    "Esurance": "Esurance",
    "FarmBureau": "FarmBureau",
    "FarmersInsurance": "Farmers",
    "Geico": "Geico",
    "KemperPreferred": "KempersUnitrin",
    "KemperSpecialty": "KempersUnitrin",
    "LibertyMutual": "LibertyMutual",
    "MercuryInsurance": "Mercury",
    "Metlife": "MetLife",
    "NationalGeneral": "NationalGeneral",
    "NationalGeneralPremier": "NationalGeneral",
    "NationalGeneralSummit": "NationalGeneral",
    "NationalGeneralValueProgram": "NationalGeneral",
    "Nationwide": "Nationwide",
    "Progressive": "Progressive",
    "Safeco": "Safeco",
    "StateFarm": "StateFarm",
    "TheGeneral": "TheGeneral",
    "TheHartford": "TheHartford",
    "Travelers": "Travelers",
    "USAA": "USAA",
    "AIG": "AIG",
    "Arrowhead": "Arrowhead",
    "Dairyland": "Dairyland",
    "DairylandAutoCycle": "Dairyland",
    "DairylandScored": "Dairyland",
    "DirectGeneral": "DirectGeneral",
    "DirectGeneralAutoInsurance": "DirectGeneral",
    "Good2goAutoInsurance": "Good2Go",
    "PlymouthRock": "PlymouthRock",
    "SafeAuto": "Safeauto",
    "SafewayInsuranceGroup": "Safeway",
    "WorkmensAutoInsurance": "Workmens",
    "Infinity": "Infinity",
    "InfinityEconomy": "Infinity",
    "InfinityRSVP": "Infinity",
    "InfinitySpecial": "Infinity",
    "Mapfre": "MAPFRE",
    "MapfreMass": "MAPFRE",
    "MapfreTronweb": "MAPFRE",
    "MapfreWA": "MAPFRE",
    "CaliforniaCasualty": "IFA",
    "Acuity": "ACUITY",
    "Gainsco": "GAINSCO"
  }
```

## Vehicle Usage

```javascript
{
  'Business Use': 'OccasionalBusinessUse',
  'Work Commute': 'CommuteToWorkOrSchool',
  'Farm Use': 'FarmUse',
  'Farm Business Use': 'FarmUse',
  Pleasure: 'DriveForPleasure',
}
```

##Vehicle Ownership

```javascript
{
  Owned: 'Owner',
  Leased: 'Leased',
  Lien: 'Financed',
}
```
## Education

```javascript
{
  'No High School Diploma': 'LessthanHighSchool',
  'High School Diploma': 'HighSchool',
  'Some College - No Degree': 'HighSchool',
  'Vocational/Technical Degree': 'Vocational',
  'Associates Degree': 'Associate',
  Bachelors: 'Bachelors',
  Masters: 'Masters',
  Phd: 'Phd',
  'Medical Degree': 'Doctor',
  'Law Degree': 'Lawyer',
}
```

## Marital Status

```javascript
{
    Single: 'Single',
    Married: 'Married',
    'Domestic Partner': 'DomesticPartner',
    Widowed: 'Widowed',
    Separated: 'Separated',
    Divorced: 'Divorced',
}
```

## Relation

```javascript
{
  Child: 'Child',
  'Domestic Partner': 'DomesticPartner',
  Insured: 'Applicant',
  Other: 'OtherRelative',
  Parent: 'Parent',
  Relative: 'OtherRelative',
  Employee: 'NonRelative',
  Spouse: 'Spouse',
}
```

## License Status

```javascript
{
  Valid: 'ValidLicense',
  Permit: 'Permit',
  Expired: 'Expired',
  Suspended: 'Suspended',
  Cancelled: 'Surrendered',
  'Not Licensed': 'NonLicensed',
  'Permanently Revoked': 'PermanentlyRevoked',
}
```

## Claim Types

```javascript
{
  Theft: 'TheftOrVandalism',
  Vandalism: 'TheftOrVandalism',
  Towing: 'SmallComprehensiveClaim',
  Glass: 'SmallComprehensiveClaim',
  Fire: 'AllOtherNonAccident',
  'Hit Animal': 'AllOtherNonAccident',
  'Tornado/Hurricane': 'AllOtherNonAccident',
  Flood: 'AllOtherNonAccident',
  'Wind/Hail': 'AllOtherNonAccident',
  'All Other': 'AllOtherNonAccident',
}
```

## Accident Types

Property Damage passed as separate argument and used in mapping

```javascript
{
  global: {
    'Not At Fault': 'NotAtFault',
    'At Fault With Injury': {
      AtFaultInjury: [0, 0],
      AtFaultInjuryAndPropertyDamage: [1, Infinity],
    },
    'At Fault With No Injury': {
      AtFaultPropertyDamageLessThan1000: [0, 1000],
      AtFaultPropertyDamagegreaterThan1000: [1000, Infinity],
    },
  },
  stateSpecific: {
    'At Fault With No Injury': {
      MA: {
        AtFaultPropertyDamageLessThan500: [0, 500],
        AtFaultPropertyDamage500To2000: [500, 2000],
        AtFaultPropertyDamageGreaterThan2000: [2000, Infinity],
      },
    },
  },
}```

## Ticket Types

```javascript
{
  global: {
    'Wrong Way/Wrong Lane': 'AllOtherMinorViolation',
    'Vehicle Theft': 'AllOtherMajorViolation',
    'Unsafe Operation of a Motor Vehicle': 'AllOtherMinorViolation',
    'Transportation of Hazardous Materials': 'AllOtherMajorViolation',
    Towing: 'AllOtherMinorViolation',
    'Ticket Violation Not Listed': 'AllOtherMinorViolation',
    Suspension: 'LicenceSuspensionOrRevocation',
    'Seat Belt': 'SeatBeltViolation',
    'Refusal to submit to chemical test': 'AllOtherMajorViolation',
    'Recreational Vehicle': 'AllOtherMinorViolation',
    'Passing School Bus': 'AllOtherMinorViolation',
    'Out of State': 'AllOtherMinorViolation',
    'Operating Vehicle without Permission': 'AllOtherMajorViolation',
    'Open Container': 'AllOtherMinorViolation',
    'Other Minor': 'AllOtherMinorViolation',
    'Other Major': 'AllOtherMajorViolation',
    'Motorcycle Violation': 'AllOtherMinorViolation',
    'Improper Loads': 'AllOtherMinorViolation',
    'Improper Passing': 'AllOtherMinorViolation',
    'Improper Parking': 'AllOtherMinorViolation',
    'Illegal Turn': 'Illegal Turn',
    Homicide: 'AllOtherMajorViolation',
    'Following too Closely': 'AllOtherMinorViolation',
    Felony: 'AllOtherMajorViolation',
    'False Reporting': 'AllOtherMajorViolation',
    'Failure to show documents': 'AllOtherMinorViolation',
    'Failure To Observe A Safety Zone': 'AllOtherMinorViolation',
    'Failure to Yield': 'AllOtherMinorViolation',
    'Failure to Stop': 'AllOtherMinorViolation',
    'Failure to Obey Signal': 'IgnoredTrafficDeviceOrSign', // AllOtherMinorViolation
    DUI: 'DuiDwi',
    'Driving too slow': 'AllOtherMinorViolation',
    'Driving Left of Center': 'AllOtherMinorViolation',
    'Double Lines': 'IgnoredTrafficDeviceOrSign', // AllOtherMinorViolation
    'Defective Equipment': 'AllOtherMinorViolation',
    'Child Safety Restraint': 'AllOtherMinorViolation',
  },
  stateSpecific: {
    'Cell Phone': {
      NV: 'HandlheldDeviceViolationFirstOffense',
      global: 'AllOtherMinorViolation',
    },

    'Racing/Drag Racing': {
      CA: 'SpeedContestDragRacing',
      global: 'AllOtherMajorViolation',
    },
    'Leaving scene of an Accident/Hit and Run': {
      CA: 'HitAndRun',
      global: 'AllOtherMajorViolation',
    },
    'Eluding Police': {
      CA: 'EvadingPolice',
      global: 'AllOtherMajorViolation',
    },
    'Driving on Sus. License': {
      CA: 'DrivingUnderSuspendedRevokedLicense',
      global: 'AllOtherMajorViolation',
    },
    'Divided Highways': {
      CA: 'DrivingOnWrongSideOfHighway',
      global: 'AllOtherMinorViolation',
    },
    'Careless Driving': {
      CA: 'RecklessDriving',
      global: 'AllOtherMajorViolation',
    },
    'Driving without lights': {
      CO: 'DefectiveOrUnsafeVehicle',
      global: 'AllOtherMinorViolation',
    },
  },
}
```

## Speeding Ticket Types

```javascript
{
  global: {
    'Speeding 1-5': 'SpeedingLessThan15Mph',
    'Speeding 6-10': 'SpeedingLessThan15Mph',
    'Speeding 11-15': 'SpeedingLessThan15Mph',
    'Speeding 16-20': 'SpeedingMoreThan15Mph',
    'Speeding 21+': 'SpeedingMoreThan15Mph',
    'Speeding Violation-Major': 'SpeedingMoreThan35MphOverPostedLimit',
    'Speeding Violation-Minor': 'SpeedingLessThan15Mph',
  },
  stateSpecific: {
    'Speed over 100mph': {
      CA: 'SpeedingOver100Mph',
      global: 'SpeedingMoreThan35MphOverPostedLimit',
    },
  },
}
```
