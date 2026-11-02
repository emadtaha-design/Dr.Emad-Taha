# Manychat integration — Dr-Emad Taha AI

## Free configuration (no code connection)
1. Connect the Facebook Page inside Manychat.
2. Automation > New automation > New trigger > **User comments on your post**.
3. Choose all eligible posts or a specific post.
4. Configure a public reply (prewritten), and attach a Messenger message node marked **Comment Reply**.
5. Test with a separate personal profile and set the flow live.

Note: Manychat may only respond publicly to the first comment per user under the trigger. The first Messenger comment reply is mandatory in the documented flow. See https://help.manychat.com/hc/en-us/articles/14281386567836-Facebook-Comments-Trigger

## AI integration (NOT available on Manychat Free)
Manychat External Request / Dynamic Block require paid plan eligibility:
https://help.manychat.com/hc/en-us/articles/14281252007580-Dev-Tools-Basics

Architecture when eligible:
Manychat comment/message trigger -> HTTPS external request -> protected AI endpoint -> response mapping -> Manychat reply.

GitHub stores source and can run scheduled jobs; it is NOT an HTTPS webhook host. Do not put API keys in GitHub source or Manychat public message fields. The previous direct Meta polling workflow is disabled to avoid duplicate replies.

## Suggested safe public response
"شكرًا لتعليقك! اكتب سؤالك بوضوح، وسنساعدك بالمعلومات المتاحة."

## Status
- Free Manychat flow: manual setup in Manychat required.
- AI bridge: not connected; requires eligible Manychat plan, hosted HTTPS endpoint and AI inference.
- No automatic comments currently published by this repository.
