FROM debian

MAINTAINER mcomet <mcomet@student.21-school.ru>

RUN apt-get update -y && apt-get upgrade -y && apt-get install libncurses5-dev groff wget vim build-essential -y

RUN wget http://downloads.sourceforge.net/project/myman/myman-cvs/myman-cvs-2009-10-30/myman-wip-2009-10-30.tar.gz && tar xvfvz myman-wip-2009-10-30.tar.gz

RUN cd myman-wip-2009-10-30 && ./configure

RUN cd myman-wip-2009-10-30 && make

RUN cd myman-wip-2009-10-30 && make install

CMD myman
