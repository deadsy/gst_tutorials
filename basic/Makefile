
CC = gcc

PACKAGE = gtk+-3.0
PACKAGE += gstreamer-1.0          
PACKAGE += gstreamer-plugins-base-1.0

#PACKAGE += gstreamer-gl-1.0
#PACKAGE += gstreamer-plugins-bad-1.0
#PACKAGE += gstreamer-tag-1.0       
#PACKAGE += gstreamer-sdp-1.0     
#PACKAGE += gstreamer-sctp-1.0             
#PACKAGE += gstreamer-controller-1.0       
#PACKAGE += gstreamer-base-1.0             
#PACKAGE += gstreamer-mpegts-1.0           
#PACKAGE += gstreamer-pbutils-1.0          
#PACKAGE += gstreamer-insertbin-1.0        
#PACKAGE += gstreamer-webrtc-1.0           
#PACKAGE += gstreamer-video-1.0            
#PACKAGE += gstreamer-allocators-1.0       
#PACKAGE += gstreamer-riff-1.0             
#PACKAGE += gstreamer-player-1.0           
#PACKAGE += gstreamer-fft-1.0              
#PACKAGE += gstreamer-bad-audio-1.0        
#PACKAGE += gstreamer-net-1.0              
#PACKAGE += gstreamer-codecparsers-1.0     
#PACKAGE += gstreamer-rtsp-1.0             
#PACKAGE += gstreamer-rtp-1.0              
#PACKAGE += gstreamer-app-1.0              
#PACKAGE += gstreamer-plugins-good-1.0     
#PACKAGE += gstreamer-check-1.0            
#PACKAGE += gstreamer-audio-1.0            

CFLAGS = -Wall -Wstrict-prototypes -Werror
CFLAGS += `pkg-config --cflags $(PACKAGE)`

LIBS = `pkg-config --libs $(PACKAGE)`

.c.o:
	$(CC) $(CFLAGS) $(INC) -c $< -o $@

TUTORIALS =  bt1 \
	bt2 \
	bt3 \
	bt4 \
	bt6 \
	bt9 \
	bt12 \
	bt13 \
	bt15 \

#	bt5 \
#	bt7 \
#	bt8 \

all: $(TUTORIALS)

$(OUT): $(OBJ)
	$(CC) -o $(OUT) $(OBJ) $(LIBS)

bt1: basic-tutorial-1.o
	$(CC) -o $@ basic-tutorial-1.o $(LIBS)

bt2: basic-tutorial-2.o
	$(CC) -o $@ basic-tutorial-2.o $(LIBS)

bt3: basic-tutorial-3.o
	$(CC) -o $@ basic-tutorial-3.o $(LIBS)

bt4: basic-tutorial-4.o
	$(CC) -o $@ basic-tutorial-4.o $(LIBS)

bt5: basic-tutorial-5.o
	$(CC) -o $@ basic-tutorial-5.o $(LIBS)

bt6: basic-tutorial-6.o
	$(CC) -o $@ basic-tutorial-6.o $(LIBS)

bt7: basic-tutorial-7.o
	$(CC) -o $@ basic-tutorial-7.o $(LIBS)

bt8: basic-tutorial-8.o
	$(CC) -o $@ basic-tutorial-8.o $(LIBS)

bt9: basic-tutorial-9.o
	$(CC) -o $@ basic-tutorial-9.o $(LIBS)

bt12: basic-tutorial-12.o
	$(CC) -o $@ basic-tutorial-12.o $(LIBS)

bt13: basic-tutorial-13.o
	$(CC) -o $@ basic-tutorial-13.o $(LIBS)

bt15: basic-tutorial-15.o
	$(CC) -o $@ basic-tutorial-15.o $(LIBS)

clean:
	-rm *.o
	-rm bt*
