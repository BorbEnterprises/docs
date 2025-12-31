---
title: All Chunk Types
description: "This page lists Pure3D chunk types found in various games created by Radical Entertainment."
---

# Introduction
This page lists Pure3D chunk types found in various games created by Radical Entertainment.

Game specific chunks on this page will be denoted with special icons:

* {{ game-icon roadrage }} The Simpsons Road Rage
* {{ game-icon hitandrun }} The Simpsons Hit & Run

Chunks that can be children of multiple other chunks will be listed under each parent chunk on this page.

# Chunk Types
* {{ game-icon roadrage }} [Grid (0x1000)](chunk-1000.md)
	* {{ game-icon roadrage }} [Grid Cell (0x1001)](chunk-1000.md#children_1001)
* {{ game-icon roadrage }} [Locator 2 (0x1003)](chunk-1003.md)
* {{ game-icon roadrage }} [Trigger Volume 2 (0x1004)](chunk-1004.md)
* {{ game-icon roadrage }} [Spline 2 (0x1005)](chunk-1005.md)
* {{ game-icon roadrage }} [NAV (0x1006)](chunk-1006.md)
* {{ game-icon roadrage }} [Intersect Mesh (0x1008)](chunk-1008.md)
	* {{ game-icon roadrage }} [Intersect Mesh 2 (0x1009)](chunk-1008.md#children_1009)
* {{ game-icon roadrage }} [Black Magic (0x1025)](chunk-1025.md)
* [Light Group (0x2380)](chunk-2380.md)
* [Mesh (0x10000)](chunk-10000.md)
* [Bounding Box (0x10003)](chunk-10003.md)
* [Bounding Sphere (0x10004)](chunk-10004.md)
* [Position List (0x10005)](chunk-10005.md)
* [Index List (0x1000A)](chunk-1000A.md)
* [Shader (0x11000)](chunk-11000.md)
    * [Shader Texture Parameter (0x11002)](chunk-11000.md#children_11002)
    * [Shader Integer Parameter (0x11003)](chunk-11000.md#children_11003)
    * [Shader Float Parameter (0x11004)](chunk-11000.md#children_11004)
    * [Shader Colour Parameter (0x11005)](chunk-11000.md#children_11005)
* [Old Billboard Quad Group (0x17002)](chunk-17002.md)
    * [Old Billboard Quad (0x17001)](chunk-17002.md#children_17001)
        * [Old Billboard Display Info (0x17003)](chunk-17002.md#children_17003)
        * [Old Billboard Perspective Info (0x17004)](chunk-17002.md#children_17004)
* [Texture (0x19000)](chunk-19000.md)
	* [Image (0x19001)](chunk-19001.md)
		* [Image Data (0x19002)](chunk-19001.md#children_19002)
* [Image (0x19001)](chunk-19001.md)
    * [Image Data (0x19002)](chunk-19001.md#children_19002)
* [Sprite (0x19005)](chunk-19005.md)
	* [Image (0x19001)](chunk-19001.md)
   		* [Image Data (0x19002)](chunk-19001.md#children_19002)
* [Animation (0x121000)](chunk-121000.md)
	* [Animation Size (0x121004)](chunk-121000.md#children_121004)
	* [Animation Group List (0x121002)](chunk-121000.md#children_121002)
		* [Animation Group (0x121001)](chunk-121000.md#children_121001)
			* [Float 1 Channel (0x121100)](chunk-121000.md#children_121100)
			* [Float 2 Channel (0x121101)](chunk-121000.md#children_121101)
			* [Vector 3D OF Channel (0x121104)](chunk-121000.md#children_121104)
			* [Quaternion Channel (0x121105)](chunk-121000.md#children_121105)
			* [Entity Channel (0x121107)](chunk-121000.md#children_121107)
			* [Boolean Channel (0x121108)](chunk-121000.md#children_121108)
			* [Colour Channel (0x121109)](chunk-121000.md#children_121109)
* {{ game-icon hitandrun }} [Road (0x3000003)](chunk-3000003.md)
* {{ game-icon hitandrun }} [Intersection (0x3000004)](chunk-3000004.md)
* {{ game-icon hitandrun }} [Locator (0x3000005)](chunk-3000005.md)
    * {{ game-icon hitandrun }} [Trigger Volume (0x3000006)](chunk-3000005.md#children_3000006)
* {{ game-icon hitandrun }} [Path (0x300000B)](chunk-300000B.md)
* {{ game-icon hitandrun }} [Set (0x3000110)](chunk-3000110.md)
* {{ game-icon hitandrun }} [Collision Effect (0x3000600)](chunk-3000600.md)
* {{ game-icon hitandrun }} [ATC (0x3000602)](chunk-3000602.md)
* {{ game-icon hitandrun }} [Static Entity (0x3F00000)](chunk-3F00000.md)
* {{ game-icon hitandrun }} [Static Phys (0x3F00001)](chunk-3F00001.md)
* {{ game-icon hitandrun }} [Intersect (0x3F00003)](chunk-3F00003.md)
* {{ game-icon hitandrun }} [Tree (0x3F00004)](chunk-3F00004.md)
    * {{ game-icon hitandrun }} [Tree Node (0x3F00005)](chunk-3F00004.md#children_3F00005)
        * {{ game-icon hitandrun }} [Tree Node 2 (0x3F00006)](chunk-3F00004.md#children_3F00006)
* {{ game-icon hitandrun }} [Fence (0x3F00007)](chunk-3F00007.md)
	* {{ game-icon hitandrun }} [Fence 2 (0x3000000)](chunk-3F00007.md#children_3000000)
* {{ game-icon hitandrun }} [Inst Stat Phys (0x3F0000A)](chunk-3F0000A.md)
* {{ game-icon hitandrun }} [World Sphere (0x3F0000B)](chunk-3F0000B.md)
* [Collision Sphere (0x7010002)](chunk-7010002.md)
* [Collision Cylinder (0x7010003)](chunk-7010003.md)
* [Collision Oriented Bounding Box (0x7010004)](chunk-7010004.md)

# Notes
This is not currently a complete list.