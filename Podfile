platform :ios, '9.0'

plugin 'cocoapods-rome'

pod "NSLogger/NoStrip", :git => "https://github.com/fpillet/NSLogger.git", :commit => "c20af3052b"

use_frameworks!

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['ENABLE_BITCODE'] = 'NO'
    end
  end
end
