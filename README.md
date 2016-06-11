troykinsella.nodejs
===================

An ansible role for installing the node.js platform from binary archive.

Dependencies
------------

* troykinsella.archive

Role Variables
--------------

* nodejs_version: Optional. The version of node.s to install. Default: 4.4.5.
* nodejs_archive_os: Optional. The target operating system. Default: linux.
* nodejs_archive_architecture: Optional. The target system architecture. Default: x64.
* nodejs_archive_file_name: Optional. The name of the archive file to download. node-v{{ nodejs_version }}-{{ nodejs_archive_os }}-{{ nodejs_archive_architecture }}.tar.xz.
* nodejs_archive_base_url: Optional. The installation archive base URL. Default: https://nodejs.org/dist/v{{ nodejs_version }}/.
* nodejs_archive_checksum: Optional. The expected installation archive checksum. Default: bd6505d8a350cd83907374ea98730b0ba99b97ec45cee418d453a0154384805a.
* nodejs_archive_checksum_algorithm: Optional. The installation archive checksum algorithm. Default: sha256.
* nodejs_archive_cache_path: Optional. The directory path into which the archive will be downloaded. Default: /usr/local/pkg.
* nodejs_archive_destination_path: Optional. The installation prefix directory path. Default: /usr/local.
* nodejs_archive_extracted_file_name: Optional. The expected name of the root file or directory that is extracted from the archive. Default: node-v{{ nodejs_version }}-{{ nodejs_archive_os }}-{{ nodejs_archive_architecture }}.
* nodejs_archive_destination_file_name: Optional. Rename the extracted directory to this value. Default: node{{ nodejs_version }}.

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: troykinsella.nodejs

License
-------

MIT
