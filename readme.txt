Admin Credentials 

email: adminuser@gmail.com
username: admin
password: 54321
phone number: 8979555556


User Credentials 






Account sid : AC7cb1dc78dc3b1a578278b411784a5e8e
Auth token: 8466e63467f9c56de3ecfc774c4af926


curl -X POST "https://verify.twilio.com/v2/Services/VA322316e2e597740802c74ddb244772b5/Verifications" \
  --data-urlencode "To=+254720554087" \
  --data-urlencode "Channel=sms" \
  -u "AC7cb1dc78dc3b1a578278b411784a5e8e:8466e63467f9c56de3ecfc774c4af926"

echo
echo -n "Please enter the OTP:"
read OTP_CODE

curl -X POST "https://verify.twilio.com/v2/Services/VA322316e2e597740802c74ddb244772b5/VerificationCheck" \
  --data-urlencode "To=+254720554087" \
  --data-urlencode "Code=$OTP_CODE" \
  -u "AC7cb1dc78dc3b1a578278b411784a5e8e:$TWILIO_AUTH_TOKEN"