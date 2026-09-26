INDIE ROYAL — COMPLETE SITE, 6 PARTS TOTAL (SMALLER THAN BEFORE)
=============================================================
This replaces the 9-part package from before. Same content, just
recompressed videos so it's fewer, lighter files to juggle. Don't mix
this with any older zip — just use this.

WHAT'S IN THIS DELIVERY
-----------------------------------------------------------------
  Part 1  -> index.html (33MB) + netlify.toml + its own README
             (this is the file from the "images embedded" package —
             it did not need to change, only the videos did)
  Part 2-6 -> assets/videos/ — hero.mp4, testimonials/, highlights/
             re-encoded to be about 40% smaller with no visible
             quality loss, and re-packed into 5 zips instead of 8.

HOW TO SET IT UP
-----------------------------------------------------------------
1. Make one new, empty folder, e.g. "indie-royal-site".
2. Unzip Part 1 into it — you get index.html and netlify.toml.
3. Unzip Parts 2 through 6 into that SAME folder, one after another.
   They only add files under assets/videos/ — nothing overlaps.
4. When done, that folder should contain:
     indie-royal-site/
       index.html          (every picture is baked inside this file)
       netlify.toml
       assets/
         videos/
           hero.mp4
           highlights/      (9 files)
           testimonials/    (6 files)
   No assets/img/ folder — that's correct. Pictures don't need one
   anymore, they're all inside index.html itself.
5. Drag that WHOLE folder onto Netlify's deploy box in one go.
6. Check Deploys → latest deploy → file list. You should see
   index.html and the full assets/videos/ tree.

ABOUT "DEPLOY IT ON NETLIFY" — WHY I CAN'T CLICK THAT BUTTON MYSELF
-----------------------------------------------------------------
I don't have your Netlify login, and I don't have a way to open a
browser or your computer from here — so I can't personally log in
and hit deploy for you. What I can do (and just did) is make the
part where you have to actually do something as small and boring as
possible: one folder, six zips to unzip into it, one drag-and-drop.
That's it — there's no other setup step hiding anywhere else.

If you'd rather not deal with zips and folders at all going forward,
the more durable fix is connecting Netlify directly to a GitHub repo
of this project (Netlify redeploys automatically on every push, no
manual drag-and-drop ever again). Happy to help set that up if you
want — just say so.

WHY VIDEOS ARE SEPARATE FILES, NOT BAKED INTO index.html
-----------------------------------------------------------------
All 144 images live inside index.html now — but the videos (about
108MB total, down from 190MB) deliberately don't. Baking them in too
would balloon index.html past 400MB, make every visitor download the
entire site's video library before the page even appears, and break
video scrubbing/seeking (only works with real separate files, which
is exactly why netlify.toml sets up byte-range support for them).
So: index.html is 100% self-contained for pictures; assets/videos/
is a real folder you deploy alongside it, once — future picture or
copy edits will never touch this videos folder again.
