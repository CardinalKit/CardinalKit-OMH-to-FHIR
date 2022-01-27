![CardinalKit Logo](https://github.com/CardinalKit/CardinalKit/raw/master/CardinalKit-Web-Assets/header.png?raw=true)

# CardinalKit Open mHealth to FHIR conversion module

This repository contains a cloud function that can be deployed to your CardinalKit firebase project that will automatically 
convert documents written to your cloud firestore in Open mHealth format into HL7 FHIR R4.

## Instructions

Log in to your Firebase account from the command line:

```firebase login```

Configure your project for the Cloud Function:

```firebase init```

Then select "Functions" >> "Use Existing Project" >> Select your Firebase project >> Choose *Javascript* as the language

Now, install dependencies:

```npm install```

Then, deploy your function:

```firebase deploy```

## Learn more

For more information, visit our website and documentation at [https://cardinalkit.org](https://cardinalkit.org).
