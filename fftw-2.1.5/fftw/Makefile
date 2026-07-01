CC =		gcc
MACHTYPE =	$(shell uname -m)
OSTYPE =	$(shell uname -s)
OBJDIR =	$(MACHTYPE)-$(OSTYPE)

$(shell mkdir -p $(OBJDIR))

CFLAGS =	-c -I. -O3 -MMD -MP

SRCS =	config.c fn_12.c fn_32.c fn_9.c  fni_15.c fni_6.c ftw_2.c ftw_7.c ftwi_32.c  ftwi_9.c twiddle.c \
	executor.c fn_13.c fn_4.c  fni_1.c fni_16.c fni_64.c ftw_3.c ftw_8.c ftwi_4.c generic.c  wisdom.c \
	fftwf77.c  fn_14.c fn_5.c  fni_10.c fni_2.c fni_7.c ftw_32.c ftw_9.c ftwi_5.c malloc.c wisdomio.c \
	fftwnd.c fn_15.c fn_6.c  fni_11.c fni_3.c fni_8.c ftw_4.c ftwi_10.c  ftwi_6.c planner.c \
	fn_1.c  fn_16.c fn_64.c fni_12.c fni_32.c fni_9.c ftw_5.c ftwi_16.c  ftwi_64.c  putils.c \
	fn_10.c fn_2.c  fn_7.c  fni_13.c fni_4.c ftw_10.c ftw_6.c ftwi_2.c ftwi_7.c rader.c \
	fn_11.c fn_3.c  fn_8.c  fni_14.c fni_5.c ftw_16.c ftw_64.c ftwi_3.c ftwi_8.c timer.c

OBJS =	$(SRCS:%.c=$(OBJDIR)/%.o)

all:	$(OBJS)

-include $(OBJS:.o=.d)

.KEEP_STATE:


$(OBJDIR)/%.o: %.c
	$(CC) $(CFLAGS) $< -o $@
