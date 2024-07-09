# LINUX_File_Management_System_Emulator <!-- omit in toc -->


This program simulates a simple Linux file system with basic shell command functionalities. It provides a structure to manage files and directories, akin to a simplified Linux environment. Below, you'll find detailed descriptions of the functionalities and commands available in this simulation.


**Table of Contents**
- [Overview:](#overview)
- [Class Descriptions:](#class-descriptions)
- [Functions:](#funtions)
- [Algorithms](#algorithms)
  - [print_tree(root, prev_struct)](#print_treeroot-prev_struct)
  - [print_ls(node=pwd->child)](#print_lsnodepwd-child)
  - [pwd_str(root, pwd)](#pwd_strroot-pwd)
  - [find_names(root, pwd, name)](#find_namesroot-pwd-name)
  - [find_on_pwd(pwd, name)](#find_on_pwdpwd-name)
  - [find_node(root, pwd, path)](#find_noderoot-pwd-path)
  - [cd(root, pwd, path)](#cdroot-pwd-path)
  - [create(root, pwd, path, type)](#createroot-pwd-path-type)
  - [remove(root, pwd, path)](#removeroot-pwd-path)
  - [dupl(root, pwd, src_path, dst_path, keep)](#duplroot-pwd-src_path-dst_path-keep)
  - [cat(root, pwd, path)](#catroot-pwd-path)
  - [edit(root, pwd, path)](#editroot-pwd-path)
  - [chmod(root, pwd, path, new_modes)](#chmodroot-pwd-path-new_modes)
- [Dry Run](#dry-run)


## Overview
The program is designed to simulate a file system using a tree structure, where each node represents either a file or a directory. It supports various commands such as ls, cd, pwd, mkdir, touch, rm, cp, mv, chmod, find, stat, edit, cat, and more, mimicking a Linux shell.
  
## Class Descriptions
TreeNode
The TreeNode class represents a node in the file system, which can either be a file or a directory.

- Attributes:
  - name: The name of the file or directory.
  - contents: The contents of the file (used for files only).
  - type: The type of node ('d' for directory, '-' for file).
  - cdate: Creation date of the node.
  - mdate: Last modified date of the node.
  - permission: Permission of the node in numeric form.
  - parent: Pointer to the parent node.
  - link: Pointer to the next sibling node.
  - child: Pointer to the first child node.
- Methods:
  - get_permission(): Returns the permission in string format (e.g., "rwx").


## Functions  
Main Functions
- linux_tree(TreeNode root):* Initializes the file system with some default directories and files.
- print_help(): Prints the help message with a list of available commands.
- print_tree(TreeNode root, string prev):* Recursively prints the contents of the directory in a tree-like format.
- print_ls(TreeNode pwd):* Lists the contents of the current directory.
- print_stat(TreeNode root, TreeNode pwd, string path):** Prints metadata of a file or directory.
- pwd_str(TreeNode root, TreeNode pwd):** Returns the current working directory as a string.
- find_names(TreeNode root, TreeNode pwd, string name):** Finds files or directories by name.
- find_node(TreeNode root, TreeNode pwd, string path):** Finds a node by its path.
- find_on_pwd(TreeNode pwd, string name):* Finds a node in the current working directory by name.
- split(string str, char delim): Splits a string by a delimiter.
- join(list<string> str, char delim): Joins a list of strings by a delimiter.
- split_name(string str): Splits a path into directory and name.
- cd(TreeNode root, TreeNode pwd, string path):** Changes the current directory.
- create(TreeNode root, TreeNode pwd, string path, char type):** Creates a new file or directory.
- remove(TreeNode root, TreeNode pwd, string path):** Removes a file or directory.
- dupl(TreeNode root, TreeNode pwd, string src, string dst, int keep):** Copies or moves a file or directory.
- edit(TreeNode root, TreeNode pwd, string path):** Edits the contents of a file.
- cat(TreeNode root, TreeNode pwd, string path):** Prints the contents of a file.
- chmod(TreeNode root, TreeNode pwd, string path, string new_modes):** Changes the permissions of a file or directory.
- clear_screen(): Clears the console screen.
