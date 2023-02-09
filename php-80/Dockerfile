FROM nicekiwi/aws-base:latest

# Install PHP 8.0
RUN amazon-linux-extras install -y php8.0

# Install PHP extensions mysqlnd,pgsql,devel,gd,mbstring,xml,bcmath,opcache,intl,pdo
RUN yum install -y php-mysqlnd php-pgsql php-devel php-gd php-mbstring php-xml php-bcmath php-opcache php-intl php-pdo php-zip

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Cleanup
RUN yum clean all