# downloads
# Download Git source code using wget or curl
wget https://github.com/git/git/archive/refs/tags/v2.40.0.tar.gz   # Replace with latest Git version
# or using curl:
curl -LO https://github.com/git/git/archive/refs/tags/v2.40.0.tar.gz   # Replace with latest Git version

# Extract the downloaded tar.gz file
tar -zxvf v2.40.0.tar.gz   # Replace with the downloaded file name

# Navigate to the extracted folder
cd git-*

# Compile Git
make prefix=/usr/local all

# Install Git
sudo make prefix=/usr/local install

# Verify the installation
git --version

# Clean up (optional)
cd ..
rm -rf git-*
rm -f v2.40.0.tar.gz   # Replace with the downloaded file name


# Download OpenSSL from GitHub (example using wget)
wget https://github.com/openssl/openssl/archive/refs/tags/OpenSSL_1_1_1k.tar.gz

# Extract the tar.gz file
tar -xvzf OpenSSL_1_1_1k.tar.gz
cd openssl-1.1.1k/

# Configure, compile, and install OpenSSL
./config
make
sudo make install

# Update the shared library cache
sudo ldconfig

# Verify installation
openssl version

# Clean up (optional)
cd ..
rm -rf openssl-1.1.1k
rm -f OpenSSL_1_1_1k.tar.gz
