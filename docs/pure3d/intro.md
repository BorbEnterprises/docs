---
title: Introduction
description: "This is general documentation of the Pure3D file format used in various games created by Radical Entertainment."
---

This is general documentation of the Pure3D file format used in various games created by Radical Entertainment.

# Format
Pure3D files are made up of at least one chunk, the root chunk. Chunks can contain other chunks, forming a hierarchy inside the file.

All chunks are at least 12 bytes and contain 3 basic pieces of information that are 4 bytes each:

* The chunk type
* The size of data inside the chunk (including the 12 bytes this is a part of)
* The entire size of the chunk itself and its child chunks (if there are any)

If the chunk has any data inside it, it is stored after these 12 bytes.

If the chunk has any children inside it, they are stored after these 12 bytes and the chunk's data.

# Chunk Types
To learn about the various chunk types that can be found in Pure3D files, see [All Chunk Types](chunk-types/all-types.md).