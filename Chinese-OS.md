# Chinese Opertating System on QubesOS
## Trying to install Chinese OS like Ubuntu Kylin as a Standalone VM

Creating  the HVM StandaloneVM *in don0*

qvm-create --class StandaloneVM \
 --property virt_mode=hvm \
 --property kernel='' \
 --label blue \
 ubentukylin-vm

