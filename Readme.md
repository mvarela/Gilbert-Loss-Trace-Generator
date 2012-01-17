# Gilbert Loss Trace Generator

Martin Varela, 2012

## Introduction 

 This program allows the generation of several accurate (with respect to
pre–defined target values) loss traces following a simplified Gilbert loss model
(2-states, one with no losses, and one with loss probability = 1). For
subjective testing, the challenge lies in getting the right stats within a few
hundred packets, as test sequences are only ~10s long. We take a
brute-force approach, generating several samples per combination of loss–rate
and mean loss burst size until enough sufficiently good traces are generated.

## Usage

You can run the program like so:

`./gilbert lr mlbs sequence_length number_of_sequences seed`

At the moment there is no proper validation of command-line arguments, so be
careful.

## Caveats

There are certain combinations of loss rate and mean loss burst size values
which are not feasible (a trivial example of this happens with `lr>50%` and
`mlbs=1`). In these cases, the program will not terminate (it can be easily
modified to do so if you need to, though).


 BECAUSE THE PROGRAM IS LICENSED FREE OF CHARGE, THERE IS NO WARRANTY
FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW.  EXCEPT WHEN
OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES
PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED
OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.  THE ENTIRE RISK AS
TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU.  SHOULD THE
PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING,
REPAIR OR CORRECTION.

 IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING
WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MAY MODIFY AND/OR
REDISTRIBUTE THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES,
INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING
OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED
TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY
YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER
PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES.


## License

This code is made available under the GNU General Public License v2.0.
