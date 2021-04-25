* Draft: 2021-04-25 (Sun)

# [Object storage](https://en.wikipedia.org/wiki/Object_storage)

> **Object storage** (also known as **object-based storage**[[1\]](https://en.wikipedia.org/wiki/Object_storage#cite_note-1)) is a [computer data storage](https://en.wikipedia.org/wiki/Computer_data_storage) architecture that manages data as objects, as opposed to other storage architectures like [file systems](https://en.wikipedia.org/wiki/File_systems) which manages data as a file hierarchy, and [block storage](https://en.wikipedia.org/wiki/Block_storage) which manages data as blocks within sectors and tracks.[[2\]](https://en.wikipedia.org/wiki/Object_storage#cite_note-2) Each object typically includes the data itself, a variable amount of [metadata](https://en.wikipedia.org/wiki/Metadata), and a [globally unique identifier](https://en.wikipedia.org/wiki/Globally_unique_identifier). Object storage can be implemented at multiple levels, including the device level (object-storage device), the system level, and the interface level. In each case, object storage seeks to enable capabilities not addressed by other storage architectures, like interfaces that are directly programmable by the application, a namespace that can span multiple instances of physical hardware, and data-management functions like [data replication](https://en.wikipedia.org/wiki/Data_replication) and data distribution at object-level granularity.
>
> Object storage systems allow retention of massive amounts of [unstructured data](https://en.wikipedia.org/wiki/Unstructured_data). Object storage is used for purposes such as storing photos on [Facebook](https://en.wikipedia.org/wiki/Facebook) (Haystack), songs on [Spotify](https://en.wikipedia.org/wiki/Spotify), or files in online collaboration services, such as [Dropbox](https://en.wikipedia.org/wiki/Dropbox_(service)).[[3\]](https://en.wikipedia.org/wiki/Object_storage#cite_note-3)

> ## Implementation
>
> ### [Cloud storage](https://en.wikipedia.org/wiki/Cloud_storage)
>
> The vast majority of cloud storage available in the market leverages is an object-storage architecture. Some notable examples are [Amazon Web Services S3](https://en.wikipedia.org/wiki/AWS_S3), which debuted in March 2006, [Microsoft Azure](https://en.wikipedia.org/wiki/Microsoft_Azure), [Rackspace](https://en.wikipedia.org/wiki/Rackspace) Files (whose code was donated in 2010 to Openstack project and released as [OpenStack Swift](https://en.wikipedia.org/wiki/OpenStack#Swift)), and [Google Cloud Storage](https://en.wikipedia.org/wiki/Google_Cloud_Storage) released in May 2010.
>
> ### Object-based file systems
>
> Some distributed file systems use an object-based architecture, where file metadata is stored in metadata servers and file data is stored in object storage servers. File system client software interacts with the distinct servers, and abstracts them to present a full file system to users and applications.
>
> ### Object-storage systems
>
> Some early incarnations of object storage were used for archiving, as implementations were optimized for data services like immutability, not performance. [EMC Centera](https://en.wikipedia.org/wiki/Content-addressable_storage) and Hitachi HCP (formerly known as HCAP) are two commonly cited object storage products for archiving. Another example is Quantum Lattus Object Storage Platform.
>
> More general-purpose object-storage systems came to market around 2008. Lured by the incredible growth of "captive" storage systems within web applications like Yahoo Mail and the early success of cloud storage, object-storage systems promised the scale and capabilities of cloud storage, with the ability to deploy the system within an enterprise, or at an aspiring cloud-storage service provider.
>
> ### Hybrid storage
>
> A few object-storage systems support Unified File and Object (UFO) storage, allowing some clients to store objects on a storage system while simultaneously other clients store files on the same storage system. While "hybrid storage" is not a widely accepted term for this concept due to the confusion with hybrid spinning disk and flash storage,[[15\]](https://en.wikipedia.org/wiki/Object_storage#cite_note-Crump-15) interoperable interfaces to the same set of data are available in some object-storage products.
>
> ### "Captive" object storage
>
> Some large Internet companies developed their own software when object-storage products were not commercially available or use cases were very specific. Facebook famously invented their own object-storage software, code-named Haystack, to address their particular massive-scale photo management needs efficiently.[[16\]](https://en.wikipedia.org/wiki/Object_storage#cite_note-haystack-16)
>
> ### Virtual object storage
>
> In addition to object-storage systems that own the managed files, some systems provide an object abstraction on top of one or more traditional filesystem based solutions. These solutions do not own the underlying raw storage, but instead actively mirror the filesystem changes and replicate them in their own object catalogue, alongside any metadata that can be automatically extracted from the files. Users can then contribute additional metadata through the virtual object storage APIs. A global namespace and replication capabilities both inside and across filesystems are typically supported.
>
> Most products in this category have recently extended their capabilities to support other Object Store solutions as well.
>
> ### Object-based storage devices
>
> Object storage at the protocol and device layer was proposed 20 years ago[*[ambiguous](https://en.wikipedia.org/wiki/Wikipedia:Please_clarify)*] and approved for the [SCSI](https://en.wikipedia.org/wiki/SCSI) command set nearly 10 years ago[*[ambiguous](https://en.wikipedia.org/wiki/Wikipedia:Please_clarify)*] as "Object-based Storage Device Commands" (OSD),[[17\]](https://en.wikipedia.org/wiki/Object_storage#cite_note-17) however, it had not been put into production until the development of the Seagate Kinetic Open Storage platform.[[18\]](https://en.wikipedia.org/wiki/Object_storage#cite_note-18)[[19\]](https://en.wikipedia.org/wiki/Object_storage#cite_note-19) The [SCSI](https://en.wikipedia.org/wiki/SCSI) command set for Object Storage Devices was developed by a working group of the SNIA for the T10 committee of the [International Committee for Information Technology Standards](https://en.wikipedia.org/wiki/International_Committee_for_Information_Technology_Standards) (INCITS).[[20\]](https://en.wikipedia.org/wiki/Object_storage#cite_note-20) T10 is responsible for all SCSI standards.

## [MinIO](https://en.wikipedia.org/wiki/MinIO)





> **MinIO** is an [Amazon S3](https://en.wikipedia.org/wiki/Amazon_S3) compatible server-side software storage stack, it can handle unstructured data such as photos, videos, log files, backups, and container images with currently the maximum supported object size of 5TB.
>
> ## Architecture
>
> MinIO storage stack has three major components: **MinIO Server**, **MinIO Client** (a.k.a. `mc`, which is a desktop client for the file management with an [Amazon S3](https://en.wikipedia.org/wiki/Amazon_S3) compatible servers), and **MinIO Client SDK** that can be used by application developers to interact with an [Amazon S3](https://en.wikipedia.org/wiki/Amazon_S3) compatible server.
>
> ### MinIO Server
>
> MinIO [cloud storage](https://en.wikipedia.org/wiki/Cloud_storage) server is designed to be minimal and scalable. It is light enough to be bundled along with the application stack, similar to [NodeJS](https://en.wikipedia.org/wiki/NodeJS), and [Redis](https://en.wikipedia.org/wiki/Redis).
>
> Designed for high performance, [peta](https://en.wikipedia.org/wiki/Petabyte) scale workloads[*[citation needed](https://en.wikipedia.org/wiki/Wikipedia:Citation_needed)*], MinIO offers a suite of features that are specific to large [enterprise deployments](https://en.wikipedia.org/wiki/Enterprise_resource_planning), these include [erasure coding](https://en.wikipedia.org/wiki/Erasure_coding), [bitrot](https://en.wikipedia.org/wiki/Data_degradation) protection, [encryption](https://en.wikipedia.org/wiki/Encryption)/[WORM](https://en.wikipedia.org/wiki/Write_once_read_many), [identity management](https://en.wikipedia.org/wiki/Identity_management), continuous [replication](https://en.wikipedia.org/wiki/Replication_(computing)), global federation, and multi-cloud deployments via gateway mode.
>
> MinIO server is hardware [agnostic](https://en.wikipedia.org/wiki/Agnostic), it can be installed on physical or virtual machines or launched as [Docker](https://en.wikipedia.org/wiki/Docker_(software)) containers and deployed on container orchestration platforms like [Kubernetes](https://en.wikipedia.org/wiki/Kubernetes),[[4\]](https://en.wikipedia.org/wiki/MinIO#cite_note-4) [Mesosphere](https://en.wikipedia.org/wiki/Mesosphere_(software)), and Docker Swarm.[*[citation needed](https://en.wikipedia.org/wiki/Wikipedia:Citation_needed)*]
>
> ### MinIO Client
>
> MinIO Client (`mc`) provides an alternative to the standard UNIX commands (e.g. `ls`, `cat`, `cp`, `mirror`, `diff`, etc) adding support for an [Amazon S3](https://en.wikipedia.org/wiki/Amazon_S3) compatible cloud storage services (AWS Signature v2 and v4).[*[citation needed](https://en.wikipedia.org/wiki/Wikipedia:Citation_needed)*] It works on [Linux](https://en.wikipedia.org/wiki/Linux), [Mac](https://en.wikipedia.org/wiki/MacOS) and [Windows](https://en.wikipedia.org/wiki/Microsoft_Windows) platforms.[*[citation needed](https://en.wikipedia.org/wiki/Wikipedia:Citation_needed)*]
>
> ### MinIO Client SDK
>
> MinIO Client SDK provides an [API](https://en.wikipedia.org/wiki/Application_programming_interface) to access any [Amazon S3](https://en.wikipedia.org/wiki/Amazon_S3) compatible object storage server.[[5\]](https://en.wikipedia.org/wiki/MinIO#cite_note-5) Language bindings are available for [Go](https://en.wikipedia.org/wiki/Go_(programming_language)), [Java](https://en.wikipedia.org/wiki/Java_(programming_language)), [Python](https://en.wikipedia.org/wiki/Python_(programming_language)), [JavaScript](https://en.wikipedia.org/wiki/JavaScript), [Haskell](https://en.wikipedia.org/wiki/Haskell_(programming_language)), and languages hosted on top of the [.NET Framework](https://en.wikipedia.org/wiki/.NET_Framework).
