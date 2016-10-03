platform :ios, '9.0'

target 'IBAnimatableBug' do

  use_frameworks!
  inhibit_all_warnings!

  pod 'IBAnimatable', '2.8.1'

end

# Podfile
post_install do |installer|
	installer.pods_project.targets.each do |target|

		if target.name == 'IBAnimatable'
      target.build_configurations.each do |config|
				config.build_settings['LD_RUNPATH_SEARCH_PATHS'] = ['$(inherited)', '/Applications/Xcode.app/Contents/Developer/Toolchains/Swift_2.3.xctoolchain/usr/lib/swift/iphonesimulator']
      end
    end
 
		target.build_configurations.each do |config|
			config.build_settings['SWIFT_VERSION'] = '2.3'
		end
	end
end
