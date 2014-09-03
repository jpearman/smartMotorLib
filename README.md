smartMotorLib
=============

A ROBOTC Library for the VEX cortex.

<pre>
<code>
/*-----------------------------------------------------------------------------*/  
/*                                                                             */  
/*                        Copyright (c) James Pearman                          */  
/*                                   2012                                      */  
/*                            All Rights Reserved                              */  
/*                                                                             */
/*-----------------------------------------------------------------------------*/
/*                                                                             */
/*    Module:     SmartMotorLib.c                                              */
/*    Author:     James Pearman                                                */
/*    Created:    2 Oct 2012                                                   */
/*                                                                             */
/*    Revisions:                                                               */
/*                V1.00  21 Oct 2012 - Initial release                         */
/*                V1.01   7 Dec 2012                                           */
/*                       small bug in SmartMotorLinkMotors                     */
/*                       fix for High Speed 393 Ke constant                    */
/*                       kNumbOfTotalMotors replaced with kNumbOfRealMotors    */
/*                       _Target_Emulator_ defined for versions of ROBOTC      */
/*                       prior to 3.55                                         */
/*                       change to motor enums for V3.60 ROBOTC compatibility  */
/*               V1.02  27 Jan 2013                                            */
/*                      Linking an encoded and non-encoded motor was not       */
/*                      working correctly, added new field to the structure    */
/*                      eport to allow one motor to access the encoder for     */
/*                      another correctly.                                     */
/*               V1.03  10 March 2013                                          */
/*                      Due to new version of ROBOTC (V3.60) detection of PID  */
/*                      version changed. V3.60 was originally planned to have  */
/*                      different motor definitions.                           */
/*                      Added the ability to assign any sensor to be used      */
/*                      for rpm calculation, a bit of a kludge as I didn't     */
/*                      want to add a new variable so reused encoder_id        */
/*               V1.04  27 June 2013                                           */
/*                      Change license (added) to the Apache License           */
/*               V1.05  11 Nov 2013                                            */
/*                      Fix bug when speed limited and changing directions     */
/*                      quickly.                                               */
/*               V1.06  3 Sept 2014                                            */
/*                      Added support for the 393 Turbo Gears and ROBOTC V4.26 */
/*-----------------------------------------------------------------------------*/
/*                                                                             */
/*    The author is supplying this software for use with the VEX cortex        */
/*    control system. This file can be freely distributed and teams are        */
/*    authorized to freely use this program , however, it is requested that    */
/*    improvements or additions be shared with the Vex community via the vex   */
/*    forum.  Please acknowledge the work of the authors when appropriate.     */
/*    Thanks.                                                                  */
/*                                                                             */
/*    Licensed under the Apache License, Version 2.0 (the "License");          */
/*    you may not use this file except in compliance with the License.         */
/*    You may obtain a copy of the License at                                  */
/*                                                                             */
/*      http://www.apache.org/licenses/LICENSE-2.0                             */
/*                                                                             */
/*    Unless required by applicable law or agreed to in writing, software      */
/*    distributed under the License is distributed on an "AS IS" BASIS,        */
/*    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. */
/*    See the License for the specific language governing permissions and      */
/*    limitations under the License.                                           */
/*                                                                             */
/*    Portions of this code are based on work by Chris Siegert aka vamfun on   */
/*    the Vex forums.                                                          */
/*    blog:  vamfun.wordpress.com for model details and vex forum threads      */
/*    email: vamfun_at_yahoo_dot_com                                           */
/*    Mentor for team 599 Robodox and team 1508 Lancer Bots                    */
/*                                                                             */
/*    The author can be contacted on the vex forums as jpearman                */
/*    email: jbpearman_at_mac_dot_com                                          */
/*    Mentor for team 8888 RoboLancers, Pasadena CA.                           */
/*                                                                             */
/*-----------------------------------------------------------------------------*/
</code>
</pre>
