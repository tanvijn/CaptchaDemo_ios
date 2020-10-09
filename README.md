# CaptchaDemo_ios
==============

A Swift project to showcase implementation of Google ReCaptcha in iOS Application.

Features
--------

1. A light weight basic wrapper to handle comunications with Google ReCaptcha decides and show caoptcha challenge on need and return callback to calling class.
2. A view controller containing a form and captchaverify button which is using this wrapper just by minimul line of code.

How to use
--------

In your project, wherever you want to show Google ReCaptcha and verify it instead of some local captcha logic. Please follow instructions mentioned below : 
1. Register on https://www.google.com/recaptcha/about/ with domain and save API key and secret generated.
2. Add wrapper CaptchaWrapper. and CaptchaWrapper.m in your project.
3. If your project is in Swift, then create Bridging Header and import CaptchaWrapper.h in that file. For more detail ![see](https://developer.apple.com/documentation/swift/imported_c_and_objective-c_apis/importing_objective-c_into_swift). If project is in Objective-c tyhen skip this step.
4. Import CaptchaWrapper.h class in your class, where you want users to validate captcha. Or import in Bridging Header(in case of Swift project).
5. In your own class initialize wrapper object like : 
            let captchaWrapper = CaptchaWrapper.init(reCaptchaWithApiKey: captchaSiteKey, baseURL: baseUrl)

Here pass Captcha public key in captchaSiteKey and url in baseURL with your domain registered on google cosole.
6. On clicking of captcha checkbox or button, call validateReCaptcha method of the wrapper. And you will get completion handler after call.

