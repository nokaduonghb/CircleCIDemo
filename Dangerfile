# ktlint check
github.dismiss_out_of_range_messages
checkstyle_format.base_path = Dir.pwd
checkstyle_format.report 'app/build/reports/ktlint/ktlintMainSourceSetCheck/ktlintMainSourceSetCheck.xml'
end

# android lint
android_lint.skip_gradle_task = true
android_lint.filtering = true
Dir["**/build/reports/lint-results*.xml"].each do |file|
  android_lint.report_file = file
  android_lint.lint(inline_mode: true)
end

# JUnit
Dir["**/build/test-results/**/TEST-*.xml", "**/build/outputs/androidTest-results/**/TEST-*.xml"].each do |file|
  junit.parse(file)
  junit.report
end
