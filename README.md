# CEPAK · LSFG
Web app for people with Parkinson's and their families: it logs levodopa doses, ON/OFF states, dyskinesias, symptoms and deep brain stimulation (DBS), 
estimates the medication effect with a model that learns from what is logged, 
and generates reports for the appointment.
Full description of the app: DESCRIPCION.mdIt's a single-page app (index.html), no installation needed. 
This repository contains only the code: it includes no patient data and no configuration for any real project.
It does not replace medical judgement.
## Try it
Open index.html in the browser. 
Without configuring anything, it works by saving the data only on that device.
### Sync between devices (optional)
Each person uses their own Firebase:Create a project in Firebase and enable Realtime Database and Google sign-in.
Copy your web app configuration and paste it into index.html, in the FB constant.
Restrict the database rules to your user. 
This is health data: do not leave the rules open.
```json
{
  "rules": {
    ".read": false,
    ".write": false,
    "pk_events": {
      ".read": "auth.uid === 'TU_UID'",
      ".write": "auth.uid === 'TU_UID'"
    },
    "pk_config": {
      ".read": "auth.uid === 'TU_UID'",
      ".write": "auth.uid === 'TU_UID'"
    }
  }
}
```
