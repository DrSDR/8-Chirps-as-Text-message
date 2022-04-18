# 8-Chirps-as-Text-message
simple matlab files that convert text to IQ file which can be sent to TX,  then another matlab script to decode IQ file recorded from SDR software.
step one, get matlab or should run in gnu octave 
step two create a simple text file.  max char is 1024char.
step three run  LFM8_TX.m script, it will pop up with asking for location of text file and will pop up where to save IQ TX file
step four  tx this iq file.  many ways use gnuradio,  or play wave file on pc and send audio to vector sig gen.
most will use gnuradio for tx.   use wav blocks in gnuradio,  then float to complex blocks  ,  
wave file is 12khz sample rate, so may need rational resampler to get iq stream to final sample rate needed for certain tx hardware.

now for the rx side
open up your favorite sdr software,  sdr#, sdrconsole, tune to tx freq.  ensure the sdr software is tuned to the center of the tx freq.
then record iq from sdr software.
should be a short recording.
then run LFM8_RX.m  to decode this wav file back to text

simple and neat project to learn about chirps, matched filter and converting bits back to text.

