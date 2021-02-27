# Steps for fastlane build running locally
## Install xcode if its not present using below command
###### xcode-select --install
## Create React native app
##### npx create-react-native-app 
###### give name as "aswanireactapp" (here in this example)
## install node modules
##### npm install expo-updates --save
##### npm install -g node-modules
## install fastlane using homebrew
###### brew install fastlane
## setup fastlane
### execute the below commands in ios folder
###### fastlane init #(select manual setup )
###### fastlane init swift
### copy the fastlane folder to root directory or directly create a folder "fastlane" in root directory and create a file named "Fastfile" inside it (both will work)
### Execute script 
###### gem install bundle
### Execute script 
###### bundle install
### if pods are not present inside ios folder install using the below commands
#### if there is no CocoaPods present install it using the below command
###### Edit Gemfile with gem "CocoaPods"
###### gem install cocoapods 
###### pod init
###### add below code inside "target 'aswanireactapp' do" section of podfile 

####### use_unimodules!
####### config = use_native_modules!
####### use_react_native!(:path => config["reactNativePath"])

###### bundle exec pod install
### set environment variable
###### export LC_ALL=en_US.UTF-8
###### export LANG=en_US.UTF-8
### create Gemfile in root directory with content 
###### source "https://rubygems.org"
###### gem "fastlane"
### Execute script 
###### bundle install
### Edit Fastline inside fastlane folder as per our requirements (refer fastlane folder inside root directory)
### Execute script for running build lane
###### bundle exec fastlane ios build

# TravisCI link
https://travis-ci.com/github/AswaniJose/reactnative-app-thanx

# Platform
ios
