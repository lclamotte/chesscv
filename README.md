# chesscv
Converts 3D chess positions to 2D representations

References:
ImageAI custom object detection tutorial: https://imageai.readthedocs.io/en/latest/customdetection/index.html

Questions/Notes:
	Should test data have 64 annotations for each square or <= 32 for pieces? 
		If each square: 
			An empty square could be represented with 0a1 (no piece on a1), 0f7 (no piece on f7)
			A white square could be wbg6 (white bishop on g6), wpc7 (white pawn c7)
			Black square would similarly be bbb3 (black bishop b3), bkb8 (black king b8), bnc6 (black knight c6)

			Then each square has an annotation of the form [team] [piece] [square]
			Could use delimiters to parse or just switch logic based on first character '0', 'w', or 'b'
	
	Eventually feed into Stockfish for live advantage graph?