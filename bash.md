# Ghostscript

## AI to PDF

    gs -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -sOutputFile=out.pdf input.ai

## AI to multiple PNG's

    gs -dNOPAUSE -dBATCH -sDEVICE=pngalpha -r72 -sOutputFile=page-%03d.png in.ai

## AI to EPS

    gs -dNOPAUSE -dBATCH -sDEVICE=eps2write -sOutputFile=out.eps input.ai
