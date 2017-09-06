#WWWWH SVG
## Who What When Why? HOW? svg
### Ben Marks

#### Precis
Why should you, as a developer care about the what and why of SVG? Join us September 11th as we dive into the structure and capabilities of SVG, and find out some of the implications to software development.


## Why should I care about SVG?
- They are _scalable_ -- for all you responsive nuts out there
- They are _XML_
    - easy to understand
- They can be manipulated _just like any other tag_
    - CSS -- YES!
    - Javascript
    - and Internal animations!
- They can hold text
- change width/height to percent or vh!
- change viewBox to what it needs to be for your view. This might be a good use of JS...


**Note: The value of a pixel depends on the view box**

**build an app for this. just press buttons. And don't switch windows 
for no reason. Always include a 'back' button.**

#### Agenda

- ~~History (10-15)~~
- Use cases:
    - Good at:
        - size: Wow! these are text files. Do a comparison.
        - responsiveness
            - Graphics do not have to be different for different screen 
            sizes and density. One file for all use-cases. These graphics 
            can also be reused on the page. And be very complex (as we will see)
        - scalability (think reuse)
        - simple animations
            - Not really designed for animation, but simple animations can 
            be accomplished and are built in (including animate along a path.)
        - building graphics on the fly
          - since the drawing is a collection of elements, you can build 
          one on the fly either in-browser, or on the server. they are 
          pretty light-weight (being "just text") 
    - Bad at:
        - IE and Edge. Everyone else is ok. There are shivs available
        - user friendliness. the complicated attributes used can be daunting
        - canvas-like activities
        - complicated animations
            - since these are essentially built in the browser, processors 
            can get bogged down with computation.
- Format and structure (15-20)
    - call up a "control file"
    - Read more about tags!
    - `<svg>`
        - attributes
    - `<g>`
    - shape and path elements
    - animation elements
    - the `xlink:href` attribute is deprecated. just use `href`
- Usage (15-20)
    - tied into the above explanation... then tie it together with a big thing.
    - make a site to contain all this!

#### What I think I know

_Forget all you know, or **think** you know_ - Willow

- **S**calable **V**ector **G**raphics
- used in CAD way back?
- based on XML
- makes more than straight lines

### History??

### Format

### Usages

#### direct manipulation?
#### d3.js definitely

#### applications?
- Custom loading icons
- Reusable graphics
- Simple 

## Slides

1. Intro - name and title
    1. Title of talk
    1. Name and background
1. Brief History
    1. Microsoft and Adobe
    1. W3C standard
1. Disadvantages
1. Advantages
    1. responsiveness
    1. size
    1. etc
1. Construction
    1. elements
    1. important tags
    1. starting off
1. Applications
    1. current uses
        - Maps!
    1. cool animation
        - NWP logo?
        - water/ocean
    1. color-blind app
        - java
          ```
            void spectral_color(double &r,double &g,double &b,double l)
                    // RGB <0,1> <- lambda l <400,700> [nm]
              {
              double t;  r=0.0; g=0.0; b=0.0;
              if ((l >= 400.0) && (l < 410.0)) { 
                t = (l - 400.0) / (410.0 - 400.0);
                r = +(0.33*t)-(0.20*t*t);
                }
              else if ((l >= 410.0) && (l < 475.0)) {
                t = (l - 410.0) / (475.0 - 410.0); 
                r = 0.14 - (0.13 * t * t);
                }
              else if ((l >= 545.0) && (l < 595.0)) { 
                t = (l - 545.0) / (595.0 - 545.0); 
                r = +(1.98 * t) - (t * t); 
                }
              else if ((l >= 595.0)&&(l < 650.0)) { 
                t = (l - 595.0) / (650.0 - 595.0); 
                r = 0.98 + (0.06 * t) - (0.40 * t * t); 
                }
              else if ((l >= 650.0) && (l < 700.0)) { 
                t = (l - 650.0) / (700.0 - 650.0); 
                r = 0.65 - (0.84 * t) + (0.20 * t * t); 
                }
              if ((l >= 415.0) && (l < 475.0)) { 
                t = (l - 415.0) / (475.0 - 415.0); 
                g = +(0.80 * t * t); 
                }
              else if ((l >= 475.0) && (l < 590.0)) { 
                t = (l - 475.0) / (590.0 - 475.0); 
                g=0.8 + (0.76 * t) - (0.80 * t * t); 
                }
              else if ((l >= 585.0) && (l < 639.0)) { 
                t = (l - 585.0) / (639.0 - 585.0); 
                g = 0.84 - (0.84 * t); 
                }
              if ((l >= 400.0) && (l < 475.0)) { 
                t = (l - 400.0) / (475.0 - 400.0); 
                b = +(2.20 * t) - (1.50 * t * t); 
                }
              else if ((l >= 475.0) && (l < 560.0)) { 
                t = (l - 475.0) / (560.0 - 475.0); 
                b = 0.7 - (t) + (0.30 * t * t); }
              }
          ```
        - COBOL
      
          ```
            if w >= 380 and w < 440:
                R = -(w - 440.) / (440. - 380.)
                G = 0.0
                B = 1.0
            elif w >= 440 and w < 490:
                R = 0.0
                G = (w - 440.) / (490. - 440.)
                B = 1.0
            elif w >= 490 and w < 510:
                R = 0.0
                G = 1.0
                B = -(w - 510.) / (510. - 490.)
            elif w >= 510 and w < 580:
                R = (w - 510.) / (580. - 510.)
                G = 1.0
                B = 0.0
            elif w >= 580 and w < 645:
                R = 1.0
                G = -(w - 645.) / (645. - 580.)
                B = 0.0
            elif w >= 645 and w <= 780:
                R = 1.0
                G = 0.0
                B = 0.0
            else:
                R = 0.0
                G = 0.0
                B = 0.0
            ```
        - VBA
            ```
            Sub Wavelength_To_RGB()
            
            'Purpose: Loop thru the wavelengths in the visible spectrum of light
            '         and output the RGB values and colors to a worksheet.
            '         Wavelength range: 380nm and 780nm
            
            Dim j As Long, CellRow As Long
            Dim R As Double, G As Double, B As Double
            Dim iR As Integer, iG As Integer, iB As Integer
            Dim WL As Double
            Dim Gamma As Double
            Dim SSS As Double
            
            
            Gamma = 0.8
            CellRow = 1
            
            For j = 380 To 780
            
              WL = j
            
              Select Case WL
            
              Case 380 To 440
                  R = -(WL - 440#) / (440# - 380#)
                  G = 0#
                  B = 1#
              Case 440 To 490
                  R = 0#
                  G = ((WL - 440#) / (490# - 440#))
                  B = 1#
              Case 490 To 510
                  R = 0#
                  G = 1#
                  B = (-(WL - 510#) / (510# - 490#))
              Case 510 To 580
                  R = ((WL - 510#) / (580# - 510#))
                  G = 1#
                  B = 0#
              Case 580 To 645
                  R = 1#
                  G = (-(WL - 645#) / (645# - 580#))
                  B = 0#
              Case 645 To 780
                  R = 1#
                  G = 0#
                  B = 0#
              Case Else
                  R = 0#
                  G = 0#
                  B = 0#
              End Select
            
              'LET THE INTENSITY SSS FALL OFF NEAR THE VISION LIMITS
              If WL > 700 Then
                 SSS = 0.3 + 0.7 * (780# - WL) / (780# - 700#)
              ElseIf WL < 420 Then
                 SSS = 0.3 + 0.7 * (WL - 380#) / (420# - 380#)
              Else
                 SSS = 1#
              End If
            
              'GAMMA ADJUST
              R = (SSS * R) ^ Gamma
              G = (SSS * G) ^ Gamma
              B = (SSS * B) ^ Gamma
            
              'Multiply by 255
              R = R * 255
              G = G * 255
              B = B * 255
            
              'Change RGB data type from Double to Integer.
              iR = CInt(R)
              iG = CInt(G)
              iB = CInt(B)
            
              'Output to worksheet
              Cells(CellRow, 1).Interior.Color = RGB(iR, iG, iB)
              Cells(CellRow, 2) = WL
              Cells(CellRow, 3) = "(" & iR & "," & iG & "," & iB & ")"
              CellRow = CellRow + 1
            
            Next j
            
            
            End Sub
            ```    
            
    1. Monty Python Animation
1. Holy god the examples!




# Take a step BACK:
1. as a developer, why do I care about SVG?
    - explore capabilities
1. as a developer, what can I do with svg, that I cannot do any other way?
    - These have some caveats
    - highlight EASE of USE and integration
1. Ok, now we HAVE to mention d3.js
    - Refer to delaine's talk.
    - go through some examples from the tutorial site
    