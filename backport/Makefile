AS		= $(CROSS_COMPILE)as
CC		= $(CROSS_COMPILE)gcc
LD		= $(CC) -nostdlib
CPP		= $(CC) -E
AR		= $(CROSS_COMPILE)ar
NM		= $(CROSS_COMPILE)nm
STRIP		= $(CROSS_COMPILE)strip
OBJCOPY		= $(CROSS_COMPILE)objcopy
OBJDUMP		= $(CROSS_COMPILE)objdump
AWK		= awk
CFLAGS		:= $(CFLAGS)
export	CROSS_COMPILE AS LD CC \
	CPP AR NM STRIP OBJCOPY OBJDUMP MAKE AWK CFLAGS

objects = ttyrun ptyrun

all: $(objects)

$(objects): %: %.c
	$(CC)  $(CFLAGS) $< -o $@
    
clean:
	/bin/rm -f *.o *~ $(objects)
