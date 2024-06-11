# 1. install tauri util
```
cargo install create-tauri-app --locked
```

# 2. prepare tauri apps

## 2.1. create sender app

### 2.1.1. create sender app from template
```
cargo create-tauri-app
✔ Project name · receiver
✔ Choose which language to use for your frontend · Rust - (cargo)
✔ Choose your UI template · Vanilla
```

### 2.1.2. change sender's identifier
```
 sender\src-tauri\tauri.conf.json
   - bundle - identifier
   > com.future-oriented-gb.local-net-metting-sender
```
   
### 2.1.3. change sender's product name
```
 sender\src-tauri\tauri.conf.json
   - package - productName
   > local-net-metting-sender
```
   
### 2.1.4. change sender's window title
```
 sender\src-tauri\tauri.conf.json
	- tauri - windows - title
	> local net metting sender
```
	
### 2.1.5. build exe and installer
```
cd sender
cargo tauri build
```

### 2.1.6. find outputs
```
exe > sender/src-tauri/target/release/local-net-metting-sender.exe
msi > sender/src-tauri/target/release/bundle/msi/local-net-metting-sender_0.0.0_x64_en-US.msi
```
	

## 2.2. create receiver app

### 2.2.1. create receiver app from template
```
cargo create-tauri-app
✔ Project name · receiver
✔ Choose which language to use for your frontend · Rust - (cargo)
✔ Choose your UI template · Vanilla
```

### 2.2.2. change receiver's identifier
```
 receiver\src-tauri\tauri.conf.json
   - bundle - identifier
   > com.future-oriented-gb.local-net-metting-sender
```
   
### 2.2.3. change receiver's product name
```
 receiver\src-tauri\tauri.conf.json
   - package - productName
   > local-net-metting-receiver
```
   
### 2.2.4. change receiver's window title
```
 receiver\src-tauri\tauri.conf.json
	- tauri - windows - title
	> local net metting receiver
```
	
### 2.2.5. build exe and installer
```
cd receiver
cargo tauri build
```

### 2.2.6. find outputs
```
exe > receiver/src-tauri/target/release/local-net-metting-receiver.exe
msi > receiver/src-tauri/target/release/bundle/msi/local-net-metting-receiver_0.0.0_x64_en-US.msi
```

