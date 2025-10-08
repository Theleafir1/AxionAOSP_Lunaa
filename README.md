downloading axionaosp sources

mkdir axionaosp
cd axionaosp
repo init -u https://github.com/AxionAOSP/android.git -b lineage-23.0 --git-lfs
repo sync

downloading lunaa sources

git clone  https://github.com/theleafir1/android_device_realme_lunaa_axionaosp.git  device/realme/lunaa

git clone  https://github.com/pjgowtham/android_device_oneplus_sm8350-common.git device/oneplus/sm8350-common

git clone https://github.com/pjgowtham/android_hardware_oplus.git hardware/oplus

git clone https://github.com/theleafir1/android_kernel_oneplus_sm8350_axionaosp.git kernel/oneplus/sm8350

git clone https://gitlab.com/pjgowtham/proprietary_vendor_realme_lunaa.git vendor/realme/lunaa

git clone https://gitlab.com/pjgowtham/proprietary_vendor_oneplus_sm8350-common.git vendor/oneplus/sm8350-common

building

./build/envsetup.sh
gk -s
axion lunaa userdebug gms pico
ax -b userdebug
