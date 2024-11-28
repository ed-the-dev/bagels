FROM dart:stable

RUN apt-get update -y && apt-get upgrade -y;

RUN apt-get install -y curl git unzip xz-utils zip libglu1-mesa

# WORKDIR /opt

ADD https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_3.24.5-stable.tar.xz .

RUN tar -xf flutter_linux_3.24.5-stable.tar.xz -C ../opt

WORKDIR /../opt

# Set environment variables
ENV FLUTTER_ROOT=/opt/flutter
ENV PATH="$FLUTTER_ROOT/bin:$PATH"

# Expose the Flutter CLI
CMD ["flutter"]