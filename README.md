# IPFS Blockchain Assignment (Assignment 1)

This assignment explains how to install IPFS, start the daemon, upload a file, retrieve its CID, and push everything to a GitHub repository using WSL (Windows Subsystem for Linux).

## Steps Performed

### 1. IPFS Installation
Kubo (IPFS) version 0.32.1 was installed using the following commands:

```bash
wget https://dist.ipfs.tech/kubo/v0.32.1/kubo_v0.32.1_linux-amd64.tar.gz
tar -xvzf kubo_v0.32.1_linux-amd64.tar.gz
cd kubo
sudo bash install.sh
```

**Screenshot:** Installation completed and version verified using `ipfs --version`

![IPFS Installation](./images/ipfs-install.png)
![IPFS Version](./images/ipfs-version.png)

---

### 2. IPFS Initialization
IPFS was initialized to generate the peer identity.

```bash
ipfs init
```

**Screenshot:** Output displaying the Peer ID and repository initialization message.

![IPFS Init](./images/ipfs-init.png)

---

### 3. Running the IPFS Daemon
The IPFS daemon was started to initialize the node.

```bash
ipfs daemon
```

**Screenshot:** Daemon started successfully with WebUI and Gateway addresses.

![IPFS Daemon](./images/daemon-start.png)

---

### 4. Uploading a File to IPFS
A file named `hello.txt` was created and added to IPFS to generate its unique content identifier (CID).

```bash
echo "Hello from Lucky!" > hello.txt
ipfs add hello.txt
```

**Screenshot:** `hello.txt` uploaded and CID displayed in the terminal.

![File Upload](./images/ipfs-add-cid.png)

---

### 5. Creating CID File
The generated CID was saved in a new file named `ipfs_cid.txt`.

```bash
echo "QmbLWQTZZspap5tE5G4taxuRhqFJayDtge58cPFEvYFi1n" > ipfs_cid.txt
```

**Screenshot:** `ipfs_cid.txt` file created with the CID.

![CID File](./images/cid-file.png)

---

### 6. Git Configuration and GitHub Repository Setup
Git was initialized and configured. The project was committed and pushed to GitHub using the following steps:

```bash
git init
git config --global user.name "Lucky Longre"
git config --global user.email "sem1luckylongre@gmail.com"
git add .
git commit -m "Added IPFS CID file for Blockchain assignment"
git branch -M main
git remote add origin https://github.com/Sem1-LuckyLongre/blockchain-assignments.git
git push -u origin main# IPFS Blockchain Assignment

This assignment explains how to install IPFS, start the daemon, upload a file, retrieve its CID, and push everything to a GitHub repository using WSL (Windows Subsystem for Linux).

## Steps Performed

### 1. IPFS Installation
Kubo (IPFS) version 0.32.1 was installed using the following commands:

```bash
wget https://dist.ipfs.tech/kubo/v0.32.1/kubo_v0.32.1_linux-amd64.tar.gz
tar -xvzf kubo_v0.32.1_linux-amd64.tar.gz
cd kubo
sudo bash install.sh
```

**Screenshot:** Installation completed and version verified using `ipfs --version`

![IPFS Installation](./images/ipfs-install.png)
![IPFS Version](./images/ipfs-version.png)

---

### 2. IPFS Initialization
IPFS was initialized to generate the peer identity.

```bash
ipfs init
```

**Screenshot:** Output displaying the Peer ID and repository initialization message.

![IPFS Init](./images/ipfs-init.png)

---

### 3. Running the IPFS Daemon
The IPFS daemon was started to initialize the node.

```bash
ipfs daemon
```

**Screenshot:** Daemon started successfully with WebUI and Gateway addresses.

![IPFS Daemon](./images/daemon-start.png)

---

### 4. Uploading a File to IPFS
A file named `hello.txt` was created and added to IPFS to generate its unique content identifier (CID).

```bash
echo "Hello from Lucky!" > hello.txt
ipfs add hello.txt
```

**Screenshot:** `hello.txt` uploaded and CID displayed in the terminal.

![File Upload](./images/ipfs-add-cid.png)

---

### 5. Creating CID File
The generated CID was saved in a new file named `ipfs_cid.txt`.

```bash
echo "QmbLWQTZZspap5tE5G4taxuRhqFJayDtge58cPFEvYFi1n" > ipfs_cid.txt
```

**Screenshot:** `ipfs_cid.txt` file created with the CID.

![CID File](./images/cid-file.png)

---

### 6. Git Configuration and GitHub Repository Setup
Git was initialized and configured. The project was committed and pushed to GitHub using the following steps:

```bash
git init
git config --global user.name "Lucky Longre"
git config --global user.email "sem1luckylongre@gmail.com"
git add .
git commit -m "Added IPFS CID file for Blockchain assignment"
git branch -M main
git remote add origin https://github.com/Sem1-LuckyLongre/blockchain-assignments.git
git push -u origin main
```

**Screenshot:** Files successfully committed and pushed to GitHub.

![GitHub Push](./images/github-push.png)

---

### 7. GitHub Repository View
The pushed files were verified on the GitHub repository page.

**Screenshot:** Repository contains `hello.txt` and `ipfs_cid.txt`.

![GitHub Repo](./images/github-repo.png)

---

## Conclusion
The assignment successfully covered the installation and execution of IPFS, file upload, CID retrieval, and GitHub integration through WSL.

**GitHub Repository**: [blockchain-assignments](https://github.com/Sem2-LuckyLongre/blockchain_assignment_1)

**View file on IPFS Gateway**:  
[https://ipfs.io/ipfs/QmbLWQTZZspap5tE5G4taxuRhqFJayDtge58cPFEvYFi1n](https://ipfs.io/ipfs/QmbLWQTZZspap5tE5G4taxuRhqFJayDtge58cPFEvYFi1n)


**Screenshot:** Files successfully committed and pushed to GitHub.

![GitHub Push](./images/github-push.png)

---

### 7. GitHub Repository View
The pushed files were verified on the GitHub repository page.

**Screenshot:** Repository contains `hello.txt` and `ipfs_cid.txt`.

![GitHub Repo](./images/github-repo.png)

---

## Conclusion
The assignment successfully covered the installation and execution of IPFS, file upload, CID retrieval, and GitHub integration through WSL.

**GitHub Repository**: [blockchain-assignments](https://github.com/Sem2-LuckyLongre/blockchain_assignment_1)

**View file on IPFS Gateway**:  
[https://ipfs.io/ipfs/QmbLWQTZZspap5tE5G4taxuRhqFJayDtge58cPFEvYFi1n](https://ipfs.io/ipfs/QmbLWQTZZspap5tE5G4taxuRhqFJayDtge58cPFEvYFi1n)


---

# Hyperledger Fabric Test Network Setup (Assignment 2)

This project explains how to set up and run a basic Hyperledger Fabric test network using its official sample repository. It includes installing the required tools, downloading the Fabric samples, and using the `network.sh` script.

---

## Prerequisites Installation

### 1. Install Go (Golang)
Go is needed to build Fabric binaries.

```bash
sudo apt install golang-go
```

**Screenshot:**

![Go Version](images/step1_go_version.png)

---

### 2. Check Docker Installation

```bash
docker --version
```

**Screenshot:**

![Docker Version](images/step2_docker_version.png)

---

### 3. Check Docker Compose Installation

```bash
docker-compose --version
```

**Screenshot:**

![Docker Compose Version](images/step3_docker_compose_version.png)

---

### 4. Verify Directory Structure

Check the current directory structure:

```bash
ls
```

**Screenshot:**

![LS Output](images/step4_ls_output.png)

---

## Cloning Fabric Samples

### 5. Clone the Fabric Samples Repository

```bash
git clone -b main https://github.com/hyperledger/fabric-samples.git
```

**Screenshot:**

![Git Clone](images/step5_git_clone.png)

---

### 6. Go to the Fabric Samples Directory

```bash
cd fabric-samples
```

**Screenshot:**

![CD fabric-samples](images/step6_cd_fabric_samples.png)

---

### 7. Download Binaries and Docker Images

```bash
curl -sSL https://bit.ly/2ysbOFE | bash -s
```

**Screenshot:**

![Download Docker Images and Binaries](images/step7_download_docker_imgaes_binaries.png)

---

## Running the Test Network

### 8. Navigate to the Test Network Folder

```bash
cd test-network
```

---

### 9. Start the Network

```bash
./network.sh up
```

**Screenshot:**

![Network Up](images/step9_network_up.png)

---

### 10. Create a Channel

```bash
./network.sh createChannel
```

**Screenshot:**

![Create Channel](images/step8_createChannel.png)

---

### 11. Shut Down the Network

```bash
./network.sh down
```

**Screenshot:**

![Network Down](images/step10_network_down.png)

---

## Conclusion

This setup shows how to install tools and run a basic Hyperledger Fabric test network. It includes starting the network, creating a channel, and stopping everything afterward.

---


# IPFS Privacy and Encryption – Command Line Assignment (Assignment 3)

This project explains how to securely upload, encrypt, decrypt, and manage file privacy using **IPFS (InterPlanetary File System)** and **OpenSSL** via the command line.

---

## Objective

The aim is to learn how to:
- Add files to IPFS
- Encrypt files using AES-256 (OpenSSL)
- Decrypt encrypted files
- Store data privately on a decentralized file system

---

## Steps

### Step 1: Create a file with sample text
```bash
echo "Hello, IPFS!" > myfile.txt
```

![Step 1](images/Step1_Create_myfile.png)

---

### Step 2: Add the original file to IPFS
```bash
ipfs add myfile.txt
```

![Step 2](images/Step2_Add_myfile_to_IPFS.png)

---

### Step 3: Encrypt the file with AES-256-CBC using OpenSSL
```bash
openssl enc -aes-256-cbc -pbkdf2 -iter 100000 -salt -in myfile.txt -out myfile_encrypted.txt -pass pass:Lucky@123
```

![Step 3](images/Step3_Encrypt_myfile.png)

---

### Step 4: Upload the encrypted file to IPFS
```bash
ipfs add myfile_encrypted.txt
```

![Step 4](images/Step4_Add_Encrypted_File_to_IPFS.png)

---

### Step 5: View the encrypted file
```bash
cat myfile_encrypted.txt
```

![Step 5](images/Step5_View_Encrypted_Content.png)

---

### Step 6: Decrypt the file using the same password
```bash
openssl enc -d -aes-256-cbc -pbkdf2 -iter 100000 -in myfile_encrypted.txt -out decrypted_file.txt -pass pass:Lucky@123
```

![Step 6](images/Step6_Decrypt_File_Success.png)

---

### Step 7: Check the decrypted content
```bash
cat decrypted_file.txt
```

![Step 7](images/Step7_Verify_Decrypted_Content.png)

---

### Step 8: Upload the decrypted file to IPFS again
```bash
ipfs add decrypted_file.txt
```

![Step 8](images/Step8_Add_Decrypted_File_to_IPFS.png)

---

## Conclusion

This task shows how to:
- Encrypt data before storing it on IPFS
- Use strong encryption to protect access
- Verify integrity by decrypting and comparing files
- Understand content-based addressing in IPFS

> **Note:** Always keep your encryption password secure to protect your data on decentralized platforms.

---

