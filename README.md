# Doorbell Hacking Workshop
Hacking a Smart Doorbell: An IoT hacking guide

## Challenge 0x01: Sniffing the WiFi password

I sniffed the communication during the setup process of my Smart Camera Doorbell. You can find the captures from Sniffle in `sniffle_ble_capture.pcap`.

<details>
  <summary>Solution</summary>
  
The credential can be found in the ATT packets with the opcode `Prepare Write request`. You can use the filter `btatt` in Wireshark.

  ```
    {
        “s”: “RogueAP”,
        “p”: “12345678”,
        “u”: “tourist8488890423”
    }
  ```
</details>

## Challenge 0x02

<details>
  <summary>Solution</summary>
  
If you follow the UDP stream, you find the file header `JFIF`. If you open the payload as image, you find images such as this.

![Alt text](images/image.png)

</details>


