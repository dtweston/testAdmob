# testAdmob
Steps to reproduce obscure Xcode + Admob + cocoapods bug :

1 - Create an empty Xcode project
2 - Add/Install `GoogleAds-IMA-iOS-SDK-For-AdMob` pod
3 - Commit everything and delete the repository from local machine
4 - Check out repository again
5 - Hit Build. Project will fail to build with error `ld: framework not found GoogleMobileAds`
6 - To fix, comment out the `GoogleAds-IMA-iOS-SDK-For-AdMob` pod and run `pod update`, then uncomment it again and run `pod update` again, project will build.
7 - If you try to commit at this point, git will pick up no changes
8 - Repeat steps 3 and 4, and you will be back at step 5
