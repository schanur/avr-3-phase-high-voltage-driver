$default_options  = {
  'target'           => ['release'],
  'c_compiler'       => ['avr-gcc'],
  'verbose_cmd'      => ['no'],
  'dry_run'          => ['no'],
  'build_root'       => ['build'],
}

desc 'Build all software components'
task      :build,           [:opt] do |t, args|
  args.with_defaults(:opt => default_options()) if args[:opt].nil?
  Rake::Task[:c_obj                ].invoke(args[:opt])
  Rake::Task[:link_binary          ].invoke(args[:opt])
end
