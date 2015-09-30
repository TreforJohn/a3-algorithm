A simple PHP demo of the world famous GSM Authentication Algorithm A3 .


Algorithm :


Encryption in the GSM network utilizes a Challenge/Response mechanism.

1) The Mobile Station (MS) signs into the network.

2) The Mobile Services Switching Center (MSC) requests 5 triples from the Home Location     Register (HLR).

3) The Home Location Register creates five triples utilizing the A8 algorithm. These five triples each contain:

> a) A 128-bit random challenge (RAND)

> b) A 32-bit matching Signed Response (SRES)

> c) A 64-bit ciphering key used as a Session Key (Kc).


4) The Home Location Register sends the Mobile Services Switching Center the five triples.

5)The Mobile Services Switching Center sends the random challenge from the first triple to the Base Transceiver Station (BTS).

6) The Base Transceiver Station sends the random challenge from the first triple to the Mobile Station.

7) The Mobile Station receives the random challenge from the Base Transceiver Station and encrypts it with the Individual Subscriber Authentication Key (Ki) assigned to the Mobile
Station utilizing the A3 algorithm.

8) The Mobile Station sends the Signed Response to the Base Transceiver Station.

9) The Base Transceiver Station sends the Signed Response to the Mobile Services Switching Center.

10)The Mobile Services Switching Center verifies the Signed Response.

11)The Mobile Station generates a Session Key (Kc) utilizing the A8 algorithm, the Individual Subscriber Authentication Key (Ki) assigned to the Mobile Station, and the random challenge received from the Base Transceiver Station.

12) The Mobile Station sends the Session Key (Kc) to the Base Transceiver Station.

13) The Mobile Services Switching Center sends the Session Key (Kc) to the Base Transceiver Station.

14) The Base Transceiver Station receives the Session Key (Kc) from the Mobile Services Switching Center.

15) The Base Transceiver Station receives the Session Key (Kc) from the Mobile Station.

16) The Base Transceiver Station verifies the Session Keys from the Mobile Station and the Mobile Services switching Center.

17) The A5 algorithm is initialized with the Session Key (Kc) and the number of the frame to be encrypted.

18) Over-the-air communication channel between the Mobile Station and Base Transceiver Station can now be encrypted utilizing the A5 algorithm.