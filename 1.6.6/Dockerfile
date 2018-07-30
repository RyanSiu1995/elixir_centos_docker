FROM ryansiu1995/erlang_centos
ENV SHELL=/bin/bash
ENV ELIXIR_VERSION=1.6.6
ENV LANG en_US.UTF-8  
ENV LANGUAGE en_US:en  
ENV LC_ALL en_US.UTF-8  

RUN mkdir /opt/elixir
RUN set -xe && wget https://github.com/elixir-lang/elixir/archive/v${ELIXIR_VERSION}.tar.gz && \
    tar -xzC /opt/elixir --strip-component=1 -f v${ELIXIR_VERSION}.tar.gz && \
    rm ./v${ELIXIR_VERSION}.tar.gz && cd /opt/elixir && make clean test
RUN ln -s /opt/elixir/bin/iex /usr/local/bin/iex && \
    ln -s /opt/elixir/bin/mix /usr/local/bin/mix && \
    ln -s /opt/elixir/bin/elixir /usr/local/bin/elixir && \
    ln -s /opt/elixir/bin/elixirc /usr/local/bin/elixirc
