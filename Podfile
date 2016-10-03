platform :ios, '9.0'

target 'IBAnimatableBug' do

  use_frameworks!
  inhibit_all_warnings!

  pod 'IBAnimatable', '2.8.1'

end

# Podfile
post_install do |installer|
	installer.pods_project.targets.each do |target|
		target.build_configurations.each do |config|
			config.build_settings['SWIFT_VERSION'] = '2.3'
		end
	end
end
