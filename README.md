# PASTE


menuentry "Bliss OS (EFI)" {
    insmod part_gpt
    insmod fat
    set root='hd1,gpt5'  # Change this if your disk layout differs
    chainloader /EFI/BlissOS/BOOTX64.EFI
}



menuentry "Bliss OS (EFI)" {
    search --no-floppy --fs-uuid --set=root 1234-ABCD
    chainloader /EFI/BlissOS/BOOTX64.EFI
}
