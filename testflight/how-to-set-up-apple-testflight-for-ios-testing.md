# How to set up Apple TestFlight for iOS testing

You need accounts on http://testflightapp.com and http://developer.apple.com


## TestFlight steps

Go to the TestFlight site and form a team:

  1. Go to http://tesflightapp.com and sign up.

  2. Create a team, e.g. "DemoTeam"

  3. Invite people and wait for them to accept.

Get the team's devices

  1. TestFlight -> People -> Actions -> Export iOS Devices

  2. The browser automatically downloads the file `testflight_devices.txt`

  3. If the downlown doesn't happen, try a different browser, or enable Flash.


## Apple steps

Go to the Apple site and register the devices:

  1. Go to http://developer.apple.com

  2. Developer -> Certificates, Identifiers & Profiles -> iOS Apps -> Devices -> All

  3. iOS Devices -> [+] -> Registering a New Device or Multiple Devices -> Register Multiple Devices -> Choose File -> choose the `testflight_devices.txt` file.

Create a provisioning profile:

  1. Download a provisioning profile.  

  2. Apply the provisioning profile to the build

  ??


## RubyMotion steps

When we use RubyMotion:

  1. Update everything and test:

    sudo rubymotion update
    brew update
    bundle update
    bundle exec rake pod:update
    bundle exec rake spec

  2. Compile and upload:

    bundle exec rake testflight notes="This is a new version"`

  3. The upload may take a while -- anywhere from a few minutes to hours.


Using TestFlight:

  * Developer enables team members to receive the build 

  * Submit and distribute 



