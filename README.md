# AI_Voice_Agent

I was exploring all the key use cases of AI voice agents and thats where found potentiality on FAQ/appoointment agents for dental clinics. Hence quickly developed an ideation how it could look like in AWS partyrock and Replitt.

![image](https://github.com/user-attachments/assets/cdb2ec88-d73d-44e9-83a6-0b3d7b329c37)

To make it formal, I decided to create a prototype if this is feasibe or not. After brief Research, I decided to go ahead on below tools to experiment.
below is the diagram.

![image](https://github.com/user-attachments/assets/5221d419-83a7-4e36-abbe-17e1b91f27f0)


The flow would be, when a patient calls a dental clinic, that number will be forwarded to a virtual number created via twilio for malaysia. The call is routed from US to malaysia since twilio servers were in US. Than via SIP trunk the call is connected virtually to internet specifically on RetellAI. RetellAI is AI voice agents that can engage in natural, human-like phone conversations(NO CODE). It’s often used for automating inbound or outbound calls. Here all the taks related to AI agent naturally written. So when the patients asks question, it uses chatgpt 4.0 mini to do reasoning and get back to eleven-labs to translate into prefered voice. So the key is to book appointment via Cal.com which is connected to google calender. Cal.com is used since it can scale to other calenders too. Than once the booking is made, the patient details, phone number, conversation, is organized and put into google sheet automatically. This automation is done via make.com where there is webhook constantly listening in RetellAI and feed into google sheet. Later Doctor's could audit this Google Sheets. Once all done it will send close and wrap up call with the patient who is in the line.

All the blueprints available in json format which can be imported into retell ai. However its not easy just to plug and play where all the tweaks to be done.
