# Passut

Passut is a simple password manager made in Python. All the Passut data is
saved in CSV format encrypted using GPG.

## Dependencies

* Some kind of program where the credentials can be piped to eg. `pbcopy` or
  `xclip`.
* [GnuPG][]
* [unicodecsv][]

## Installation

1. Install GnuPG and some pipe program
2. Install unicodecsv. You might need to be root in order to do this.
   `pip install unicodecsv`
3. Install [passut.py][] into your path, and make it executable.
4. Run passut.py once in order to generate a new configuration file.
5. In your home directory there is a file `.passut.cfg`. Set your settings
   there.

## Usage

Passut takes two parameters: a command and an (optional) name. The way name
behaves depends on the command. The commands are:

* `get`, `g`: Search for a password with given name and pipe it to pipe
  command.
* `save`, `s`: Save a password with given name (the wizard will ask the rest).
* `list`, `l`: List password names by given group name.

## Examples

Search for a password that starts with "foobar" and pipe it to pipe command:

    $ passut.py get foobar

Save a password with a name "example":

    $ passut.py save example

List password names where the group name starts with "important":

    $ passut.py list important

## License

(2-clause BSD license)

Copyright (c) 2014, Jaakko Pallari
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this
list of conditions and the following disclaimer.
* Redistributions in binary form must reproduce the above copyright notice,
this list of conditions and the following disclaimer in the documentation
and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

[unicodecsv]: https://github.com/jdunck/python-unicodecsv
[gnupg]: http://gnupg.org/
[passut.py]: https://raw2.github.com/jkpl/passut/master/passut.py
