# How to remove zip folders visible in explorer
create a .reg file with the following content

```
Windows Registry Editor Version 5.00
; Disable ZIP folders
[-HKEY_CLASSES_ROOT\CompressedFolder\CLSID]

[-HKEY_CLASSES_ROOT\SystemFileAssociations\.zip\CLSID]

; Disable CAB folders
[-HKEY_CLASSES_ROOT\CABFolder\CLSID]

[-HKEY_CLASSES_ROOT\SystemFileAssociations\.cab\CLSID]

```

After a reboot the folders will be gone


Putting them back

```
Windows Registry Editor Version 5.00
; Enable ZIP folders
[HKEY_CLASSES_ROOT\CompressedFolder\CLSID]
@="{E88DCCE0-B7B3-11d1-A9F0-00AA0060FA31}"

[HKEY_CLASSES_ROOT\SystemFileAssociations\.zip\CLSID]
@="{E88DCCE0-B7B3-11d1-A9F0-00AA0060FA31}"

; Enable CAB folders
[HKEY_CLASSES_ROOT\CABFolder\CLSID]
@="{0CD7A5C0-9F37-11CE-AE65-08002B2E1262}"

[HKEY_CLASSES_ROOT\SystemFileAssociations\.cab\CLSID]
@="{0CD7A5C0-9F37-11CE-AE65-08002B2E1262}"

```