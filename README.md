# fdroid-submission-checklist

Personal checklist before package submittion in fdroid

* check for name conflicts
* move all signing code into signingConfig for simpicity
* add fastline structure
* upgrade gradle:

    for example
    
      ./gradlew wrapper --gradle-version 7.3.3 \
      
        --gradle-distribution-sha256-sum b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302

* tag release as versonName
* create new branch in fork of fdroiddata with name as app id
* add the file metadata/{app_id}.yml
* add:

    prebuild:
    
      - sed -i -e '/signingConfig/d' build.gradle
      
* remember to say there is git submodules, makes life easier for everyone
