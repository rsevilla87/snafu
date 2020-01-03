FROM centos/tools

USER root
RUN rpm -ivh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN yum install -y makefile gcc libaio-devel zlib-devel                                                 
RUN git clone https://github.com/axboe/fio.git --depth=1                                                
RUN cd fio && make && make install
RUN yum install -y git python-pip
RUN pip install --upgrade pip
RUN pip install elasticsearch numpy configparser statistics
RUN mkdir -p /opt/snafu/
COPY . /opt/snafu/
