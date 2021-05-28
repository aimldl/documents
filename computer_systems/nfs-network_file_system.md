* Draft: 2021-04-26 (Mon)

# NFS (Network File System)

NFS is a protocol used by Unix-like OSs (Unix, Linux, macOS, FreeBSD, etc.).

## Basics

> ### Whats is NFS?
>
> **Network File System** (**NFS**) is a [distributed file system](https://en.wikipedia.org/wiki/Distributed_file_system) protocol originally developed by [Sun Microsystems](https://en.wikipedia.org/wiki/Sun_Microsystems) (Sun) in 1984,[[1\]](https://en.wikipedia.org/wiki/Network_File_System#cite_note-sun85-1) allowing a user on a client [computer](https://en.wikipedia.org/wiki/Computer) to access files over a [computer network](https://en.wikipedia.org/wiki/Computer_network) much like local storage is accessed. NFS, like many other protocols, builds on the [Open Network Computing Remote Procedure Call](https://en.wikipedia.org/wiki/Open_Network_Computing_Remote_Procedure_Call) (ONC RPC) system. NFS is an open standard defined in a [Request for Comments](https://en.wikipedia.org/wiki/Request_for_Comments) (RFC), allowing anyone to implement the protocol.
>
> Source: [Network File System](https://en.wikipedia.org/wiki/Network_File_System), Wikipedia

> ### How does NFS work?
>
> To access data stored on another machine, i.e. a server, the server would implement NFS daemon processes to make data available to clients. The server administrator determines what to make available and ensures it can recognize validated clients.
>
> From the client's side, the machine requests access to exported data, typically by issuing a mount command. If successful, the client machine can then view and interact with the file systems within the decided parameters.
>
> Source: [Network File System (NFS)](https://www.extrahop.com/resources/protocols/nfs/)

### Versions and Variations

* NFSv2
* NFSv3
* NFSv4
* Other extensions
  * WebNFS:  an extension to Version 2 and Version 3

### Platforms

> NFS is often used with [Unix](https://en.wikipedia.org/wiki/Unix) operating systems (such as [Solaris](https://en.wikipedia.org/wiki/Solaris_(operating_system)), [AIX](https://en.wikipedia.org/wiki/AIX), [HP-UX](https://en.wikipedia.org/wiki/HP-UX)), Apple's [macOS](https://en.wikipedia.org/wiki/MacOS), and [Unix-like](https://en.wikipedia.org/wiki/Unix-like) operating systems (such as [Linux](https://en.wikipedia.org/wiki/Linux) and [FreeBSD](https://en.wikipedia.org/wiki/FreeBSD)). It is also available to operating systems such as Acorn [RISC OS](https://en.wikipedia.org/wiki/RISC_OS),[[14\]](https://en.wikipedia.org/wiki/Network_File_System#cite_note-Sunfish/Moonfish_by_Alex_Waugh-14) [AmigaOS](https://en.wikipedia.org/wiki/AmigaOS), the [classic Mac OS](https://en.wikipedia.org/wiki/Classic_Mac_OS), [OpenVMS](https://en.wikipedia.org/wiki/OpenVMS),[[3\]](https://en.wikipedia.org/wiki/Network_File_System#cite_note-NFSforVMS-3) [MS-DOS](https://en.wikipedia.org/wiki/MS-DOS),[[15\]](https://en.wikipedia.org/wiki/Network_File_System#cite_note-PCNFS-15) [Microsoft Windows](https://en.wikipedia.org/wiki/Microsoft_Windows),[[16\]](https://en.wikipedia.org/wiki/Network_File_System#cite_note-SFU-16) [OS/2](https://en.wikipedia.org/wiki/OS/2),[[17\]](https://en.wikipedia.org/wiki/Network_File_System#cite_note-17) [ArcaOS](https://en.wikipedia.org/wiki/ArcaOS),[[18\]](https://en.wikipedia.org/wiki/Network_File_System#cite_note-18) [Novell NetWare](https://en.wikipedia.org/wiki/Novell_NetWare),[[19\]](https://en.wikipedia.org/wiki/Network_File_System#cite_note-NFSforNetWare-19) and IBM [AS/400](https://en.wikipedia.org/wiki/AS/400).[[20\]](https://en.wikipedia.org/wiki/Network_File_System#cite_note-OS/400-NFS-20) Alternative remote file access protocols include the [Server Message Block](https://en.wikipedia.org/wiki/Server_Message_Block) (SMB, also termed CIFS), [Apple Filing Protocol](https://en.wikipedia.org/wiki/Apple_Filing_Protocol) (AFP), [NetWare Core Protocol](https://en.wikipedia.org/wiki/NetWare_Core_Protocol) (NCP), and OS/400 File Server file system (QFileSvr.400).
>
> SMB and [NetWare Core Protocol](https://en.wikipedia.org/wiki/NetWare_Core_Protocol) (NCP) occur more often than NFS on systems running Microsoft Windows; AFP occurs more often than NFS in Apple [Macintosh](https://en.wikipedia.org/wiki/Macintosh) systems; and QFileSvr.400 occurs more often in [AS/400](https://en.wikipedia.org/wiki/AS/400) systems. [Haiku](https://en.wikipedia.org/wiki/Haiku_(operating_system)) in 2012 added NFSv4 support as part of a Google Summer of Code project.
>
> Source: [Network File System](https://en.wikipedia.org/wiki/Network_File_System), Wikipedia