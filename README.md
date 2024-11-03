# Comprehensive Software Installation Guide for macOS

## 1. Homebrew Installation
Homebrew is a package manager for macOS that makes it easy to install and manage software.

### Install Homebrew
1. Open the Terminal.
2. Run the following command:

   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

3. Follow the on-screen instructions to complete the installation.

### Verify Homebrew Installation
Check the installation by running:

```bash
brew --version
```

## 2. Java Installation and Configuration
### Install OpenJDK
1. Open the Terminal.
2. Run the command to install OpenJDK:

   ```bash
   brew install openjdk
   ```

### Verify Java Installation
Check the Java version with:

```bash
java --version
```

### Configure jenv for Java Version Management
1. Install jenv:

   ```bash
   brew install jenv
   ```

2. Add OpenJDK to jenv:

   ```bash
   jenv add /usr/local/opt/openjdk/libexec/openjdk.jdk
   ```

3. List installed jenv versions:

   ```bash
   jenv versions
   ```

4. Set the global Java version:

   ```bash
   jenv global <version>
   ```

## 3. PostgreSQL Installation
### Install PostgreSQL
1. Install PostgreSQL using Homebrew:

   ```bash
   brew install postgresql@17
   ```

### Start PostgreSQL Service
To start PostgreSQL and have it run at login:

```bash
brew services start postgresql@17
```

### Verify PostgreSQL Installation
Check the PostgreSQL version with:

```bash
psql -V
```

## 4. pgAdmin 4 Installation
### Install pgAdmin 4
1. Install pgAdmin 4 using Homebrew:

   ```bash
   brew install --cask pgadmin4
   ```

### Launch pgAdmin 4
You can find pgAdmin 4 in your Applications folder. Launch it, and when prompted, enter your PostgreSQL credentials (username: `postgres`, password: your specified password).

### Verify pgAdmin 4 Installation
Once launched, ensure that you can connect to your PostgreSQL server using the credentials you set up.

## 5. Git Installation
### Install Git
1. Install Git using Homebrew:

   ```bash
   brew install git
   ```

### Verify Git Installation
Check the Git version with:

```bash
git --version
```

## 6. Docker Installation
### Install Docker
1. Install Docker using Homebrew:

   ```bash
   brew install --cask docker
   ```

### Verify Docker Installation
Check the Docker version with:

```bash
docker --version
```

## 7. Kafka Installation
### Install Kafka
1. Install Kafka using Homebrew:

   ```bash
   brew install kafka
   ```

### Start Kafka and Zookeeper
Start Zookeeper:

```bash
zookeeper-server-start /usr/local/etc/kafka/zookeeper.properties
```

Start Kafka:

```bash
kafka-server-start /usr/local/etc/kafka/server.properties
```

## 8. AWS CLI Installation
### Install AWS CLI
1. Update Homebrew:

   ```bash
   brew update
   ```

2. Install AWS CLI:

   ```bash
   brew install awscli
   ```

### Verify AWS CLI Installation
Check the AWS CLI version with:

```bash
aws --version
```

### Configure AWS CLI
Run the following command to set up your AWS credentials:

```bash
aws configure
```

### Install eksctl
1. Install eksctl:

   ```bash
   brew install eksctl
   ```

2. Verify eksctl Installation:

   ```bash
   eksctl version
   ```

### Install kubectl
1. Install kubectl:

   ```bash
   brew install kubectl
   ```

2. Verify kubectl Installation:

   ```bash
   kubectl version --client
   ```

---

