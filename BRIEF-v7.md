moneycanbuy.fun: shoot RAW FOOTAGE for a 30-second promo. You deliver raw material only, each piece as a separate file: no edit, no text, no logos, no music, no voice. We add all words, logos, site UI and the edit ourselves afterwards. Read BRIEF-v7.md in this repository (this same text) and the toad-head/ folder. Ignore BRIEF.md, reference/, ui/ and logos/: they belong to an earlier job in a different format.

TOOLS: every clip must come from a real video generation model, image-to-video: first make a photoreal start still, then animate it. If you have no video generation model, do NOT substitute code animation, slideshows, pans over stills or morphing stills: deliver what you can make honestly and say so in README.md.

STYLE: photoreal live action, like real phone footage people post: natural daylight or warm indoor light, true colors, shallow depth of field, real skin and fabric texture, no cartoon, no 3D render look, no cinematic grading.

A) CLIPS. MP4, H.264, no audio track. Vertical, the native size of the model: 1080x1920 preferred, never below 720x1280, do not upscale, state the native size in the README. 4-5 s each, 24-30 fps. Photoreal, natural motion, mostly steady camera with a slight handheld feel. NO LETTERS ANYWHERE in any frame: blank cups, blank papers, blank signs, blank menu boards, no names under video tiles. Props we will put words on later (cups, check, sign, carton, receipt) must stay rigid and keep their shape, never melt or morph. Every phone shown has a SOLID BRIGHT GREEN #00FF00 screen, flat and evenly lit, no glare, no reflections, no UI, facing the camera, all four screen edges and corners unobstructed (a thumb may touch the middle).
01 Coffee shop: a barista in a plain green apron (no logo) grabs and marks many blank white cups fast with a capped marker, so the cups stay pure white; a queue of customers watches. Modern coffee shop, no logos, no mermaid or round emblem anywhere.
02 Fast food: a young man wearing a big plush mascot head of OUR toad orders at a red-and-yellow fast-food counter, the staff stare at him. The head is exactly as toad-head/front.png and toad-head/three-quarter.png (see OUR TOAD). Must not look like any real burger restaurant: no crowns, no arches, no clown; menu boards blank or pictures of food only.
03 Bank: a man in a suit slams a giant blank paper check (about 1 m wide, plain cream paper, no lines, no print) onto a marble bank counter, the banker is shocked. A marble investment-bank lobby with an LED ticker strip on the wall showing only abstract green and red bars and arrows, no letters, no numbers.
04 Skate: a skater kickflips over a big chalk frog drawing on asphalt, friends cheer. The chalk frog is a simple doodle, no words. The kickflip must really happen, board and feet clean.
05 Subway: inside a subway car a person holds up a large BLANK white sign with both hands, held still at chest height; passengers raise phones and film. No route maps or ads with text.
06 Ice water: a person stands looking at a phone (green screen, see above, screen toward the camera); a friend steps in and dumps a bucket of ice water on them, splash, gasp.
07 Milk: a person pours a plain white milk carton (blank front panel) over their own head, then turns to the camera with a deadpan look and a milk moustache.
08 Video call: a laptop screen with a video call grid, a whole team and the boss (bigger tile, wears a tie) all wearing simple green frog masks, no text; people nod and move. No app interface, no names, no buttons with words.
09 Phone, one hand: a hand holds a green-screen phone, the thumb scrolls up, then taps once in the middle.
10 Phones, several: several hands each hold a green-screen phone and tap at once.
11 Phone still: one hand holds a green-screen phone still, slow slight push-in.

B) STILLS. PNG, 2048 px on the long side, photoreal, NO text or logo anywhere, even soft lighting, object facing the camera, flat readable surfaces we can put words on:
S1 a row of 10 blank white coffee cups on a counter;
S2 a barista apron chest, plain green, with a blank flat patch area;
S3 a blank giant paper check lying flat on marble, seen from above;
S4 a blank receipt hanging out of a register printer;
S5 a blank white subway sign held up in a subway car, square to the camera;
S6 a plain white milk carton with a blank front panel.
Also deliver the start still you made for every clip 01-11 (PNG, full size), we use them for compositing.

OUR TOAD: the only costume is a HUMAN wearing our toad as a big plush mascot head, copied from toad-head/front.png and toad-head/three-quarter.png: flat toad green, heavy half-closed lids over cream eyes, a wide flat smirk, small nostrils, dark spots on the cheeks, a gold chain with a gold "$" tag on the chest, always visible. Build the start still from these references (image reference or image-to-image), never from a generic frog. Never round or googly eyes, never wide open eyes, never film the head from behind. The "$" on the tag is the only symbol allowed in the whole delivery. Frog masks in clip 08 are simple frog masks, not our toad.

PEOPLE AND BRANDS: no real brands, no logos, no real or famous faces, no celebrities. Mixed ordinary people, natural clothes without prints.

C) README.md: one row per delivered file with the tool and model used, the exact prompt used, the native resolution, fps and length, and any file that failed and was regenerated (and why). contact-sheet.png: every clip as 3 frames (start, middle, end) labelled by file number (labels allowed on the contact sheet only), plus all stills, in one image.

REJECTION LIST, check every file before delivery and regenerate anything that fails:
1. Letters, numbers or logos anywhere (signs, cups, screens, clothes, ticker, video tiles), except the "$" on the toad tag.
2. A phone screen that is not solid #00FF00, has glare or UI, or has a covered edge or corner.
3. Morphing faces, hands, fingers or props; props changing shape.
4. Frozen or near-still clips, slideshows, code animation.
5. Wrong toad head: generic frog, round eyes, missing chain or "$" tag, seen from behind.
6. Clips shorter than 4 s, upscaled clips, text or watermarks from the generator.
7. A real brand look, a real person's face.
Write the result of this check in the README, one line per item with the files checked.

FILES, exactly these names under artifacts/: clips/01.mp4 to clips/11.mp4, stills/S1.png to stills/S6.png, start/01.png to start/11.png, README.md, contact-sheet.png.

The files may be used, changed and published by moneycanbuy.fun without attribution; say so in the README.
