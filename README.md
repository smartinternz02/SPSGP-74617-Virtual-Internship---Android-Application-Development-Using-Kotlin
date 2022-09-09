# SPSGP-74617-Virtual-Internship---Android-Application-Development-Using-Kotlin
Virtual Internship - Android Application Development Using Kotlin
AccountAddressTigger:
trigger AccountAddressTrigger on Account (before insert,before update) {
for(Account account:Trigger.New){
if(account.Match_Billing_Address__c==True){
account.ShippingPostalCode=account.BillingPostalCode;
}
}
}
