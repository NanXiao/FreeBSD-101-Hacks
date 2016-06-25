Print PCI devices info
----
`FreeBSD` provides `pciconf` command which can list `PCI` devices info:  

    # pciconf -lv
    hostb0@pci0:0:0:0:  class=0x060000 card=0x197615ad chip=0x71908086 rev=0x01 hdr=0x00
    vendor = 'Intel Corporation'
    device = '440BX/ZX/DX - 82443BX/ZX/DX Host bridge'
    class  = bridge
    subclass   = HOST-PCI
    pcib1@pci0:0:1:0:   class=0x060400 card=0x00000000 chip=0x71918086 rev=0x01 hdr=0x01
    vendor = 'Intel Corporation'
    device = '440BX/ZX/DX - 82443BX/ZX/DX AGP bridge'
    class  = bridge
    subclass   = PCI-PCI
    isab0@pci0:0:7:0:   class=0x060100 card=0x197615ad chip=0x71108086 rev=0x08 hdr=0x00
    vendor = 'Intel Corporation'
    device = '82371AB/EB/MB PIIX4 ISA'
    class  = bridge
    subclass   = PCI-ISA
    ......

If you are accustomed to `lspci` which is shipped on `GNU/Linux`, you can install it yourself:  

	# pkg install pciutils
	......
	# lspci
	00:00.0 Host bridge: Intel Corporation 440BX/ZX/DX - 82443BX/ZX/DX Host bridge (rev 01)
	00:01.0 PCI bridge: Intel Corporation 440BX/ZX/DX - 82443BX/ZX/DX AGP bridge (rev 01)
	00:07.0 ISA bridge: Intel Corporation 82371AB/EB/MB PIIX4 ISA (rev 08)
	......

Reference:  
["lspci" & pciconf commands in FreeBSD](http://kazaonfreebsd.blogspot.com/2012/12/lspci-pciconf-commands-in-freebsd.html).