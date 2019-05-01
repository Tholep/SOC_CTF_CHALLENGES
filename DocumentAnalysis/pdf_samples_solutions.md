============================================================================
file: 0000fc3840119cade9fb2dae9576cafd3be7f923
original hash: 0000fc3840119cade9fb2dae9576cafd3be7f923
desc: 2stages, simple obfuscation

deobfuscation:
1) peepedf:	js_beautify object 7 > stage1.js
2) atom:	fix the syntax issues
3) atom: line 27: adjo -> print
4) $: 		v8 stage1.js > stage2.js
5) peepdf: 	js_analyze file stage2.js

results:

	Attack vectors:
		depends on Adobe PDF reader version:
			< 8.11 collab_email();
			< 8.13 util_printf();
			< 9.1 collab_geticon();
			
	URLs in shellcode:
		http://analistikyandeks.cn/dfjmu2.exe
		http://analistikyandeks.cn/efotx2.exe
		http://analistikyandeks.cn/djqsu2.exe

=============================================================================
file: 00060c6f8c34a29e9aa4b87e1f00f87b38389a27
original hash: 00060c6f8c34a29e9aa4b87e1f00f87b38389a27
desc: >3 stages, hard obfuscation

deobfuscation:
- next time

=============================================================================
file: 007e8ec8a52033a66c21d114a169dd556766d98b
original hash: 007e8ec8a52033a66c21d114a169dd556766d98b
desc: 1 stage, simple obfuscation

deobfuscation:
1) peepdf: 	js_beautify object 7 > stage0.js
2) $:		v8 stage0.js > stage1.js
3) peepdf: 	js_analyze file stage2.js

results:
	URLs in shellcode:
		http://greenlpl.com/exe.php?spl=PDF%20(printd)
		http://greenlpl.com/exe.php?spl=PDF%20(EmailInfo)
		http://greenlpl.com/exe.php?spl=PDF%20(util_printf)
		http://greenlpl.com/exe.php?spl=PDF%20(GetIcon)


=============================================================================
file: 008452447522f0c79d51c2a33ec66ff5146740a1
original hash: 008452447522f0c79d51c2a33ec66ff5146740a1
desc:

deobfuscation:
1) peepdf: 	js_beautify object 7 > stage0.js
2) nano line 22,23: change gkmov for print funtion
3) $ 		v8 stage0.js > stage1.js

results:
	URLs in shellcode:
		http://style-boards.com/forum/bilsxy2.exehttp://style-boards.com/forum/click.php?r=
		http://style-boards.com/forum/bfikt2.exehttp://style-boards.com/forum/click.php?r=
		http://style-boards.com/forum/cgikmo2.exehttp://style-boards.com/forum/click.php?r=

	attack vectors:
		<8.12  collab_email();
		<8.13  util_printf();
		<9.1   collab_geticon();


============================================================================
file: 003fddfdf2c321cbc9aa58ec41ed8b9b13f9394e
original file name: 003fddfdf2c321cbc9aa58ec41ed8b9b13f9394e
desc: pre & post filters usage, CVE-2010-0188 - hard to conclude

deobfuscation:
1) js_beautify object 1 > stage0.js
2) nano add caw="";
3) nano line 685: print("p:",p);
3) v8 -f pre.js stage0.js // -f post.js 
4) copy shellcode to file shell.bin
5) js_unescape file shell.bin



URLs in shellcode:
	http://amesearch.info/tre/LENA.py






	


