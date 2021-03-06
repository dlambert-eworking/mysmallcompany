# CIS Benchmarks : Exemple d'audit scripté d'une politique sécurité sous GCP
source : 
  * Benchmark : Google Cloud Computing Platform from https://www.cisecurity.org/cis-benchmarks/
  * Audit tool : https://github.com/GoogleCloudPlatform/inspec-gcp-cis-benchmark
  * Ruby Install : https://linuxize.com/post/how-to-install-ruby-on-centos-7/

prerequisit :
* Chef : c'est une version free de chef qui a été utilisée pour le test. See https://www.chef.io/end-user-license-agreement/.


##  Install Ruby
Les repos Centos ne permettent que d'installer une version obsolètesde ruby
voir "Install Ruby using Rbenv" ([ref 3]) pour installer une version compatible avec la version nécessaire de Chef

##  Launch CIS Benchmarks

```Shell
  inspec exec https://github.com/GoogleCloudPlatform/inspec-gcp-cis-benchmark.git -t gcp:// --input gcp_project_id=data-proc-test-dla  --reporter cli json:data-proc-test-dla_scan.json
```

```Shell  
  Profile: Google Cloud Platform Resource Pack (inspec-gcp)
Version: 1.7.0
Target:  gcp://default

     No tests executed.

Profile Summary: 4 successful controls, 19 control failures, 20 controls skipped
Test Summary: 35 successful, 49 failures, 83 skipped
  
```
