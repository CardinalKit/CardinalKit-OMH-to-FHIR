![CardinalKit Logo](https://github.com/CardinalKit/CardinalKit/raw/master/CardinalKit-Web-Assets/header.png?raw=true)

# CardinalKit Open mHealth to FHIR conversion module

This repository contains a [Firebase Cloud Function](https://firebase.google.com/products/functions) that can be deployed to your CardinalKit Firebase project to automatically 
convert documents written to your Cloud Firestore in [Open mHealth](https://openmhealth.org) format by the CardinalKit iOS application into [HL7 FHIR R4 Observation Resources](https://www.hl7.org/fhir/observation-examples.html). Mapping is based on the [Open mHealth to HL7 FHIR Implementation Guide](https://healthedata1.github.io/mFHIR/).

## Instructions

Before using this function, you will need to have created a CardinalKit mobile app and connected it to a Firebase backend. If you haven't done this yet, please follow the instructions [here](https://cardinalkit.org/cardinalkit-docs/1-cardinalkit-app/1-start.html) first. Then you can return and add the cloud functions to your Firebase project by following the directions below.

Log in to your Firebase account from the command line:

```
firebase login
```

Clone this repository, then open it in the terminal and configure your firebase project for the Cloud Function:

```
cd CardinalKit-OMH-to-FHIR/firebase
firebase init
```

Then select "Functions" >> "Use Existing Project" >> "Select your Firebase project" >> Choose *Javascript* as the language.

Now, install dependencies:

```
npm install
```

Then, deploy the included functions:

```
firebase deploy --only functions
```

If the installation succeeded, you will see a new `HealthFhir` subcollection appear for each user in your Cloud Firestore that your app collects HealthKit data for which will contain all your OMH data converted to FHIR Observations. 

## Learn more

For more information, visit our website and documentation at [https://cardinalkit.org](https://cardinalkit.org).
