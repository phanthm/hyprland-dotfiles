#!/bin/bash

function send_notification() {
    current_brightness=$(brightnessctl g)
    max_brightness=$(brightnessctl m)
    percentage=$((current_brightness * 100 / max_brightness))
    dunstify -a "brightness" -u low -r 9994 -h int:value:"$percentage" -i "brightness" "Brightness: ${percentage}%" -t 2000
}

case $1 in
up)
    brightnessctl s 5%+
    send_notification $1
    ;;
down)
    brightnessctl s 5%-
    send_notification $1
    ;;
esac
