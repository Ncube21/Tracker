# Tracker



import smtplib
 
text = "You are being watched"
 
ml = smtplib.SMTP ('smtp.gmail.com',587)
 
ml.ehlo()
 
ml.starttls()
 
ml.login('your-email','password')
 
#Now here comes the fun part.
#Let's say you want your boss
#to think he got the mail from CIA.
#Type in like nobody@cia.com in place of 
#foremail and your boss's email in place
#of receiver.
 
ml.sendmail('foremail','receiver',text)
 
ml.close()

Execute and Hit “Run”. BOOM!! 
Well, now if you want to bomb his mailbox, just loop it.

while True:
    ml.sendmail('foremail','receiver')
