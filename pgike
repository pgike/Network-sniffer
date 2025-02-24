from scapy.all import *

# Define the packet callback function
def packet_callback(packet):
    if packet.haslayer(IP):
        ip_src = packet[IP].src
        ip_dst = packet[IP].dst
        protocol = packet[IP].proto

        print(f"Packet captured: {ip_src} -> {ip_dst}, Protocol: {protocol}")

        # If the packet has a TCP layer, display details
        if packet.haslayer(TCP):
            tcp_srcport = packet[TCP].sport
            tcp_dstport = packet[TCP].dport
            print(f"TCP Packet: {ip_src}:{tcp_srcport} -> {ip_dst}:{tcp_dstport}")

        # If the packet has a UDP layer, display details
        elif packet.haslayer(UDP):
            udp_srcport = packet[UDP].sport
            udp_dstport = packet[UDP].dport
            print(f"UDP Packet: {ip_src
