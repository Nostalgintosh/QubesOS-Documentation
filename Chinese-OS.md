# Chinese Opertating System on QubesOS
## Trying to install Chinese OS like Ubuntu Kylin as a Standalone VM

The Reason? To get into another world of the internet and exlpore the internet that another countery have to offer. Seeing another lens that other countries can not see and use. By leveraging the open source, you can get in the Chinese Internet, and bypass the The Great FireWall of China.

Creating  the HVM StandaloneVM *in don0*

qvm-create --class StandaloneVM \
 --property virt_mode=hvm \
 --property kernel='' \
 --label blue \
 ubentukylin-vm

