# FtpSync.sh
# Michael Hutter, 20.11.2021
# This Script can be used to synchronize a remote FTP directory and a local directory

HOST='ftp.mywebspace.de'
USER='web1234567f1'
PASS='YourSecretPwd'
SERVERFOLDER='/FolderOnWebspace'
PCFOLDER='/home/michael/ftpsync/MyLocalFolder'
CopyMoreThanOneFileSimultaneously="--parallel=10"

CopyServerdataToLocal=1 # 0=Upload, 1=Download
IgnoreSubdirectories=1
ContinuePartiallyTransmittedFiles=0
DontOverwriteNewerExistingFiles=0 # If this is used ContinuePartiallyTransmittedFiles will not work!

DeleteAdditionalFilesInDestinationDir=0 # Deletes files in DestDir which are not present in SourceDir
RemoveSourceFilesAfterTransfer=0 # Moves the files instead of copying them

ExcludeParams='--exclude-glob .* --exclude-glob .*/' # Exclude (hidden) files and direcories -> starting with a dot

OnlyShowChangesButDontChangeFiles=0 # DryRun mode
OutputAsMuchInfoAsPossible=1 # Verbose mode
