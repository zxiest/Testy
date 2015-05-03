# -*- coding: utf-8 -*-
$:.unshift("/Library/RubyMotion/lib")
require 'motion/project/template/ios'

begin
  require 'bundler'
  Bundler.require
rescue LoadError
end

require 'motion-cocoapods'

Motion::Project::App.setup do |app|
  # Use `rake config' to see complete project settings.
  app.name = 'Testy'

  app.pods do
    pod 'Facebook-iOS-SDK', '~> 4.0.0'#, '~> 3.16.0'
  end

  FB_APP_ID = '1558527791076765'
  app.info_plist['FacebookAppID']   = FB_APP_ID
  app.info_plist['CFBundleURLTypes'] = [{ CFBundleURLSchemes: ["fb#{FB_APP_ID}"] }]
  app.info_plist['Application requires iPhone environment']=true
  app.info_plist['URL types'] = { 'URL Schemes' =>"fb#{FB_APP_ID}"}
end
