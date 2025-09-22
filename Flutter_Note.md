# Install 
```
sudo snap install flutter --classic
```

# Download 

```
curl -fsSL https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_3.24.5-stable.tar.xz -o flutter.tar.xz
```


# Unzip

```
tar xf flutter.tar.xz
```



# Export path

```
export PATH="$PATH:`pwd`/flutter/bin" && flutter --version
```


### Go to Project --> export path -->> Check flutter doctor

```
cd /home/nazmul/Desktop/PrivecyApp/privacy_app_flutter && export PATH="$PATH:`pwd`/../flutter/bin" && flutter doctor
```

### Run

```
cd /home/nazmul/Desktop/PrivecyApp/privacy_app_flutter && export PATH="$PATH:`pwd`/../flutter/bin" && flutter run -d chrome --web-port=8080
```
