# Xamarin 101 Workshop

## Exercise 4 - App Center and Github

1 - Go to the link and add AppCenter app to your github repo.

<https://github.com/marketplace/app-center>

2 -- Setup the app instalation:\
<https://github.com/settings/installations>

3 -- You will be redirected to the AppCenter Page, login and Select the
repo you want to create CI/CD for.

4 -- Configure the App center App

5 -- On the Visual studio AndroidProject Set the Build to Release and
archive the app for publishing (We will create now the KeyStore file)

6 -- Select the Archived app and Click the bottom right corner button
where it says Sign and Distribute:

7 -- Click in Create a new key and fill the form (SAVE THE PASSWORD)

8 -- Click in Publish the app and save the certificate in your desktop
or your git repo

9 -- Fill the Password that you added in the Past form

10 -- Get the certificate acconting to this document

<https://docs.microsoft.com/en-us/xamarin/android/deploy-test/signing/index?tabs=macos#newcertxs>

11 - Select the Branch you want to configure the CD/CI, and add the
Keystore here:

<https://docs.microsoft.com/en-us/xamarin/android/deploy-test/signing/index?tabs=macos#newcertxs>

12 -- Add the keystore alias and passwords, and trigger a build
