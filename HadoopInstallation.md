To verify Hadoop releases using GPG:

    Download the release hadoop-X.Y.Z-src.tar.gz from a mirror site.
    Download the signature file hadoop-X.Y.Z-src.tar.gz.asc from Apache.
    Download the Hadoop KEYS file.
    gpg --import KEYS
    gpg --verify hadoop-X.Y.Z-src.tar.gz.asc
