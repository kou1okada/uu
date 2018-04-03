# uu - USB Utilities for Linux

# Usage
~~~
Usage: uu [OPTIONS ...] COMMAND [ARGS ...]
Commands:
  cat [PATHS]        cat attributes
  ls [PATHS]         List devices and attributes
  realpath [PATHS]   Show realpath

  chpower DEV STATE  Change power state
  power [DEV]        Show power state

  bind DRIVER DEV    Bind driver to device
  ls-bind [DEV]      List drivers binded to device
  ls-driver [PATHS]  List drivers and binds
  unbind [DEV]       Unbind driver from device

Options:
  -h,--help
~~~

For more details, use -h options for each subcommand.

# Examples for usage
~~~
# List devices
uu ls

# List attributes of device
uu ls 6-1

# Cat a attribute
uu cat 6-1/{id*,serial}

# List drivers binded to device
uu ls-bind 6-1

# Show power state
uu power 6-1

# Suspend device
uu chpower 6-1 auto
uu unbind 6-1

# Resume device
uu bind usb 6-1

# Suspend/Resume device by aliases
uu suspend 6-1
uu resume 6-1
~~~
