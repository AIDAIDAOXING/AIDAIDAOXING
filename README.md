AIDAIDAOXING
/
AIDAIDAOXING

Type / to search

Code
Pull requests
Actions
Projects
Security
Insights
Settings
Settings: AIDAIDAOXING/AIDAIDAOXING
Access
Code and automation
Security
Integrations
Runners / Add new self-hosted runner · AIDAIDAOXING/AIDAIDAOXING
Adding a self-hosted runner requires that you download, configure, and execute the GitHub Actions Runner. By downloading and configuring the GitHub Actions Runner, you agree to the GitHub Terms of Service or GitHub Corporate Terms of Service, as applicable.

Runner image

macOS

Linux

Windows
Architecture
Download
Win-arm64 runners are currently in pre-release status and subject to change.

We recommend configuring the runner under "\actions-runner". This will help avoid issues related to service identity folder permissions and long path restrictions on Windows.

# Create a folder under the drive root
$ mkdir actions-runner; cd actions-runner# Download the latest runner package
$ Invoke-WebRequest -Uri https://github.com/actions/runner/releases/download/v2.309.0/actions-runner-win-arm64-2.309.0.zip -OutFile actions-runner-win-arm64-2.309.0.zip# Optional: Validate the hash
$ if((Get-FileHash -Path actions-runner-win-arm64-2.309.0.zip -Algorithm SHA256).Hash.ToUpper() -ne '114d11ba8b95c22946c642cc9190c2214f6a2da60c2996ae26e2d9dc176f994e'.ToUpper()){ throw 'Computed checksum did not match' }# Extract the installer
$ Add-Type -AssemblyName System.IO.Compression.FileSystem ; [System.IO.Compression.ZipFile]::ExtractToDirectory("$PWD/actions-runner-win-arm64-2.309.0.zip", "$PWD")
Configure
# Create the runner and start the configuration experience
$ ./config.cmd --url https://github.com/AIDAIDAOXING/AIDAIDAOXING --token BC4IVDU5DBZ467SRSZJDCALFCU7YG# Run it!
$ ./run.cmd
Using your self-hosted runner
# Use this YAML in your workflow file for each job
runs-on: self-hosted
For additional details about configuring, running, or shutting down the runner, please check out our product docs.

Footer
© 2023 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
