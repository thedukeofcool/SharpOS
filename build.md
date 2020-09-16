# Buliding SharpOS

To build SharpOS type in these commands:<br>
```i686-elf-gcc -T linker.ld -o os.bin -ffreestanding -O2 -nostdlib boot.o kernel.o -lgcc```<br>```grub-file --is-x86-multiboot os.bin```<br>```mkdir -p iso/boot/grub```<br>
```cp os.bin iso/boot/os.bin```<br>```cp grub.cfg iso/boot/grub/grub.cfg```<br>```grub-file --is-x86-multiboot os.bin iso```<br>```qemu-system-i386 -cdrom os.iso```
