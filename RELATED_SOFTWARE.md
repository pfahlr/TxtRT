ASCII/ANSI Art Editors and Winamp-Style Visualizer Preset Tools
Master Catalog of Tools
Below is a compiled inventory of notable tools in two domains: (A) ASCII/ANSI/Text Art Editors & Toolchains (including character art formats like PETSCII, teletext, etc.), and (B) Winamp-Style Audio Visualization Preset Ecosystems. Each tool entry is categorized and annotated with key attributes (platforms, license, status, etc.). This catalog is delivered in both CSV and JSON formats for further analysis. CSV Schema (columns): name, category, primary_formats, license, open_source, repo_url, homepage_url, platforms, status, first_release, last_release, price, core_features, notable_limitations, export_options, import_options, web_rendering_support, community_metrics, docs_quality, examples_or_screenshots, notes


[RELATED_TOOLS.PDF](./RELATED_TOOLS.PDF)
[TECH_STACK_OPTIONS.PDF](./TECH_STACK_OPTIONS.PDF)

Key observations from the matrix:

Advanced drawing features: Modern text editors like REXPaint and Moebius offer brushes, shapes, and even half-block painting (Moebius) for finer detail
blocktronics.github.io
. Layers remain relatively rare – REXPaint and upcoming tools like Icy Draw support layers, addressing a frequent request for complex compositions (users on Reddit were excited about layers in Icy Draw). Selection and transformation (move/rotate/flip) are common in GUI editors (PabloDraw, Moebius, RexPaint), though absent in terminal-based ones.

Character set and Unicode support: Older tools are tied to code page 437, whereas newer ones see demand for Unicode (e.g. Durdraw mixing CP437 with Unicode braille blocks
github.com
, and a user wishlist explicitly called out Unicode glyph support
reddit.com
). MoebiusXBIN takes this further by allowing custom fonts/encodings, effectively any Unicode symbol set
blog.glyphdrawing.club
. This is a clear trend: modern ASCII art apps must go beyond CP437 to include box-drawing, block elements, and even emoji.

Palette and color: All ANSI editors handle the classic 16 colors; many now also handle extended palettes (256-color ANSI, truecolor). For instance, Durdraw supports both 16-color ANSI and 256-color xterm mode
github.com
, and RexPaint even has a full RGB picker
curlie.org
. Dithering tools (for converting images to ASCII) exist externally and sometimes internally (Playscii has some dithering filters). Palette management (loading C64 palettes, custom ANSI palettes, etc.) is increasingly important (MoebiusXBIN includes many palettes
blog.glyphdrawing.club
).

Canvas size and performance: New editors are built to handle very large text canvases (hundreds of lines/columns): Moebius and Icy Draw leverage GPU acceleration (OpenGL) to scroll/zoom smoothly, overcoming old DOS limits
saul.pw
. Playscii and RexPaint also handle large images with ease. This addresses the historical 100-line barrier in TheDraw
saul.pw
 – modern artists expect to create much bigger pieces (e.g., for posters or animated ANSI).

Collaboration & version control: PabloDraw pioneered multi-user editing over TCP/IP (multi-cursor in the same canvas)
facebook.com
, which remains unique. Most other tools are single-user. However, with ASCII art often being a niche, real-time collab isn’t common, though it’s a potential differentiator for a new app (especially given the success of collaborative coding and design tools).

Animation support: Frame-based animation in text art is now a reality in tools like Durdraw
github.com
 and Playscii (which can onion-skin between frames for ASCII GIF creation). This resurrects the “ANSiMation” concept in a modern way. Expect demand for this as ASCII art is used in creative videos or terminal animations.

Automation and scripting: Very few text art editors support scripting – Playscii has a Python API, and some command-line tools like FIGlet/boxes can be scripted in pipelines. This is an area of opportunity (e.g., batch-processing images to ASCII, algorithmic art generation).

Export and integration: Modern ASCII/ANSI editors typically provide image export (PNG) for sharing on the web (since not all platforms can render .ANS correctly) – often via Ansilove or internal routines. HTML export (with CSS for colors) is also seen (Durdraw, ASCII Art Paint). Embeddable viewers: some editors (PabloDraw, sixteencolors.net) rely on web libraries to display art – a strong candidate for a new project is a built-in web viewer (perhaps leveraging canvas or WebGL for perfect fidelity, like Ansilove.js).

Accessibility: Text art inherently can be accessible (as it’s text), but the editors themselves need considerations (keyboard navigation, high contrast UI, screen reader labels). Most older tools are keyboard-driven (by necessity on DOS/terminal), which is good, but UIs were not designed with screen readers in mind. A modern editor could capitalize on this by ensuring UI controls are accessible and perhaps offering assistive features (like describing ANSI art out loud – a challenge but notable).

Visualizer tools special notes: For Winamp-style visualizers, the “features” differ. The preset editors (MilkDrop, AVS) are more like IDEs for generative graphics:

MilkDrop 2’s “editor” is essentially a real-time code editor for shader-like scripts
pawelporwisz.pl
, so no brushes or GUI aids – a gap noted by users (authoring MilkDrop presets has a high learning curve
pawelporwisz.pl
). Some have dreamed of node-based or GUI tools for MilkDrop presets; none have fully materialized, though projectM’s team has discussed GUI editors (and one can imagine integrating a Shadertoy-like interface).

AVS had a GUI for selecting effect components, but it’s dated. No modern visual preset creation tool exists with a friendly UI, representing an opportunity. Community interest is evidenced by attempts like WebVS and forum discussions on making preset creation easier.

Audio-reactivity is a given in these, but ease of use and cross-platform playback are what recent projects address (projectM and Butterchurn enabling use outside Winamp). A new tool focusing on visualizer preset editing could combine the intuitiveness of AVS’s building blocks with the power of MilkDrop’s shaders.

In summary, the feature matrix shows that no single tool yet ticks all the boxes. For ASCII/ANSI art, an ideal modern editor would combine: multi-layer compositing, high-zoom canvas, Unicode + custom fonts, integrated figlet/boxes, animation support, and collaboration – none of which are all in one product (Icy Draw and Moebius are getting close, but still evolving). In the visualization realm, there’s a clear gap for a cross-platform preset editor (not just player) that could lower the bar for creating those mesmerizing graphics.

Market Brief
Landscape Summary

Text Mode Art Revival: ASCII/ANSI art, once a necessity of BBS culture, has become a retro-nostalgic art form sustained by passionate communities. Platforms like 16colo.rs (an archive for new and old ANSI/ASCII art) and events at demoparties (text mode graphics compos) show continued interest. The scene is vibrant albeit niche:

Communities & Groups: Long-standing art groups (ACiD, iCE) wound down in early 2000s
en.wikipedia.org
, but new collectives like Blocktronics (founded 2008) carry the torch
en.wikipedia.org
. There’s cross-pollination with the demoscene (many ANSI artists are demosceners and vice versa). The Mistigris group and Discord servers (e.g., “Artscene” Discord) host active discussions. Subreddits like r/ANSIart and r/bbs are small but active, indicating a resurgence of interest among tech nostalgists and young artists experimenting with the style.

Tools Maturity: We now have both historical tools (TheDraw, ACiDDraw – useful for inspiration but only run in DOS/emulators) and modern ones (PabloDraw, Moebius, etc.). Modern tools are mostly freeware or open-source, often labors of love by lone developers or small teams. A few commercial exceptions exist (Monodraw on Mac, primarily targeting diagramming rather than ANSI art enthusiasts). Many open-source projects see sporadic development, often when the maintainer is personally interested (e.g., Moebius by Andy Herbert with last updates in 2023, Durdraw by cmang still active, Icy Draw just emerged in 2023).

Cross-platform expectation: Unlike in the ’90s (when ANSI art was mostly made on DOS), today’s users demand editors for Windows, macOS, and Linux alike. Cross-platform frameworks (Qt, .NET 5/6, Electron) have enabled this – PabloDraw leveraged .NET Core, Moebius uses C++/SDL, etc. Web-based editors are also gaining traction for accessibility (no install needed) – e.g., ASCII Art Paint, ASCIIFlow for quick diagrams, and various image-to-ASCII converters online.

Usage & Users: ASCII/ANSI art creation now falls into a few niches:

Art packs and galleries: Enthusiasts still release periodic “artpacks” (often in .zip files containing .ANS, .NFO, .TXT with SAUCE metadata) reminiscent of the BBS era. These packs are curated on 16colo.rs and similar sites. Newcomers often discover ANSI art through these archives or via social media, then seek tools to try it themselves.

Roguelike and game dev: Ascii art editors like RexPaint have found a secondary market in indie game development (for prototyping roguelike graphics, designing levels with text symbols, etc.). This increases demand for features like multi-layer, high resolution, custom tilesets, which pure BBS ANSI editors historically didn’t need.

Developers/DevOps: A subset uses ASCII diagramming tools (e.g., Monodraw, ASCIIFlow) for technical documentation, because text diagrams fit version control and code reviews well. This is adjacent to the ANSI art scene but has different requirements (monochrome, box drawing characters, etc.). It shows a market for “text graphics” beyond just art – any modern tool that can straddle diagramming and art (with modes or templates for each use-case) could capture both audiences.

What’s Missing / Gaps:
Despite the variety of tools, certain gaps are evident:

Unified Feature Set: Many tools excel in some areas and lack others. For example, one might have networking collab but no Unicode support, another has Unicode but no GUI. There isn’t yet a one-stop editor that ticks all the requested features the community has voiced (like the list of “must-haves” on Reddit: Unicode, 256-color, layers, cross-platform terminal mode
reddit.com
).

Ease of Use vs. Capability: Some modern editors (e.g. Moebius) aim to mimic the feel of pro design software (Photoshop-like), which can be complex for newcomers. Conversely, old tools are simple but limited. There’s room for a tool with progressive complexity – easy to start drawing ASCII, but with advanced panels for layers, scripting, etc. as you need them.

Integration with Modern Workflow: The ability to easily share creations on modern platforms is crucial. That means export to web-friendly formats (SVG for crisp vector-text, PNG for bitmap snapshot, even animated GIF/video for ANSI animations). Not all tools handle that well yet (some rely on external converters). A modern editor bundling a high-quality exporter (like a built-in Ansilove engine or similar) would save users hassle. Also, developers might want to generate ASCII art as part of build processes (for readme files or console output graphics) – a scriptable CLI for the editor or library form could tap into that demand.

Ecosystem & Formats: Alongside editors, there are ancillary components:

Fonts & Encoding Resources: Websites like int10h.org (VileR’s archive of text mode fonts) are important for reference – artists want their art to look right with the proper fonts. Tools that incorporate these (like MoebiusXBIN including VileR’s fonts
blog.glyphdrawing.club
, or Icy Draw supporting .TDF TheDraw fonts) are appreciated.

Metadata (SAUCE): Preservation of SAUCE tags (which store title, author, group, date, etc.) is considered good practice in the scene. Modern editors all try to support it. It’s a selling point if your tool properly reads/writes SAUCE – avoids the nightmare of someone losing attribution info after editing in a tool that ignores it.

Conversion & Viewing: Tools like Ansilove, and viewer apps like iNFekt, are part of the pipeline. While not “creative” tools, they ensure art can reach audiences. Any new editor would ideally integrate or bundle such viewers or converters to simplify the user’s workflow (e.g., a one-click “export as PNG” or a live HTML preview panel for the ANSI art).

Audio Visualization Ecosystem (Winamp-style Visuals):

The “preset” communities peaked in the Winamp era (2000s) with massive libraries of presets shared via forums like Winamp Forums (MilkDrop forum threads still exist) and DeviantArt (e.g., AVS presets in groups like AVSociety). After Winamp’s decline, these communities shrank, but notable fragments remain:

projectM has a community of open-source enthusiasts (as seen on their GitHub and Discord) trying to keep these visuals alive on new music players.

Visbot is a group dedicated to archiving and continuing AVS preset creation (they even put AVS 2.82 source on GitHub and made minor updates).

A niche of electronic music streamers and VJs still use MilkDrop (or projectM) for live visuals. For example, tools like Kaleidosync (a MilkDrop-based VJ tool) existed, and Butterchurn integration in online radio or DJ apps is happening.

There’s a new interest in using these visuals in creative coding: e.g., the HuggingFace MilkDrop LLM mentioned in links suggests experimentation with AI-generated presets – a sign that people still find the concept intriguing and worth exploring with modern tech.

Modern Relevance: The resurgence of Winamp (the brand is relaunching) and projects like Webamp (a full Winamp in the browser) bring nostalgia visuals to new audiences. Butterchurn has made it trivial to embed MilkDrop in any web page; we’re seeing it used as a “cool background” on websites, in music web players, etc. So MilkDrop presets are finding a second life on the web. However, AVS presets (which are more CPU heavy and Windows-tied) haven’t enjoyed such a revival – they remain more of an underground, preserved art form.

Opportunity: No one has yet built the “Figma for music visualizers” – a modern app to graphically create and tweak these audio-reactive visuals, share them, maybe even interface with music streaming. Given how popular visualizers are in video content (think Spotify’s Canvas feature or YouTube audio-reactive visuals), there’s potential to modernize the preset concept to a broader creative tool (beyond Winamp). MilkDrop’s tech (per-pixel shaders reacting to FFT of music) was ahead of its time. Today, with WebGL, shaders are mainstream (e.g., Shadertoy community). A modern UI on top of something like Butterchurn could attract a new generation to preset-making, framing it almost like a game or creative coding platform.

Social & Nostalgia Trends:

We’re firmly in an era where the aesthetics of the 80s/90s (pixel art, VHS glitches, text-mode graphics) are retro cool. ANSI art fits into this trend (for example, we see ANSI-style illustrations in zines, album covers, even fashion). The demoscene has “Oldskool” textmode competitions, and events like Blockparty had ANSI/ASCII compos. Teletext art had a mini-revival (e.g., art shows displaying teletext pages on old TVs). These are small scale but indicate a general cultural appreciation.

Streaming & Video – people streaming themselves coding or gaming sometimes use ASCII art generators to decorate their streams. The Matrix “digital rain” (effectively green text art) is a pop culture icon. All this to say, text art has a mainstream appeal when packaged right (see how fast an “ASCII filter” can go viral on social media). A modern tool might succeed by not just targeting the old BBS crowd, but also new users who are after the aesthetic for their creative projects.

Competitive Highlights:

Open Source vs Commercial: In ASCII/ANSI editors, open-source/free reigns – the target user base expects tools to be free (and many are hobby projects anyway). Commercial attempts like Monodraw are rare and succeed by targeting a different market (macOS power users, diagramming) rather than the art scene directly. Similarly, in visualizers, projectM and Butterchurn (open) have effectively superseded any need for a paid product (the original Winamp MilkDrop was free with Winamp). One exception: some mobile visualizer apps based on projectM sell for a few dollars on app stores – indicating casual users might pay a bit for convenience on their phone/TV.

Quality and Continuity: A lot of current tools are maintained but not heavily developed. This means a new entrant with robust features could capture attention, especially if the developer engages with the community for feedback (the Icy Draw dev asking Reddit for input is a great example
reddit.com
 – it built goodwill and ensured features matched real needs like the BBS line-length option
reddit.com
). Being responsive to such niche needs (e.g., supporting PCB @X codes for BBS, or special PETSCII quirks) can quickly make a tool the favored one among enthusiasts.

Integration with Platforms: One competitive edge could be integrating with modern platforms – e.g., a text art editor that can post directly to Twitter with proper formatting, or a visualizer tool that can ingest Spotify or microphone input easily and output to OBS for streamers. Those are outside the scope of “traditional” tools but align with how people might want to use them today.

In summary, the market is niche but global – pockets of users across the US, Europe (especially Scandinavia for demoscene, Eastern Europe for teletext, etc.), and pockets in South America and Asia (Shift-JIS art in Japan remains a thing on textboards). A modern cross-platform editor that is open-source (or affordable) and embraces this culture could become the central tool of a modest-sized but passionate market. It’s not about huge revenue, but about dominating the niche and possibly spilling over to adjacent niches (like diagramming or VJing visuals), as the user mentioned.

Trends and Opportunities

Web-based Creation and Sharing: As seen with web apps like ASCII Art Paint and the popularity of Butterchurn’s website, lowering the friction to create and share is key. An app that runs in the browser (or has a companion web app) can attract casual users. Imagine a web gallery where people can draw ANSI art collaboratively or a site where users remix MilkDrop presets visually – these could spur a renaissance in content creation. There is an opportunity to integrate creation tools with online galleries/communities (for example, a direct export from an editor to 16colo.rs, or an online preset repository).

Cross-pollination between ASCII art and code art: The rise of creative coding (Processing, p5.js, Shadertoy) shows people love to create visually with code. ASCII art and visualizer presets both sit at an intersection of programming and art. Marketing a modern tool as a creative coding platform (with a gentler learning curve) could attract users from that sphere. E.g., include a scripting engine (Lua or Python) to manipulate the ASCII canvas or generate patterns algorithmically – now your tool is also appealing to generative artists.

Social media formats: Perhaps support exporting ANSI art as animated SVG or even as an HTML5 canvas snippet that can be embedded. For visualizers, providing templates to easily make music videos (say, import an audio file and auto-generate a video with chosen preset) could open a use-case for indie musicians who want cool visuals without mastering AfterEffects.

Educational angle: These tools also teach programming concepts (MilkDrop presets teach about shaders and math; ASCII art can teach thinking in grids). There might be a minor opportunity in educational tech – e.g., a simplified visualizer editor used in a digital art class to demonstrate sound-reactive programming, or an ASCII art tool to teach image processing (when converting pictures to ASCII). While not a primary market, it’s a way to broaden appeal.

Competitors Overview:

In ASCII art editors: The main “competitors” to a new project are Moebius (open, actively improved), PabloDraw (stable, widely used but not evolving much), and newcomers like Icy Draw. A new entrant would need to outdo them in features or UX. Given Moebius’s strong foundation, one strategy could be to build on it (it’s open source Apache2) – e.g., contribute features or fork if needed (like MoebiusXBIN did). The community often consolidates around a few key tools to avoid fragmenting too much. If your features are unique (say, real-time collaboration or a built-in web publishing), that could differentiate strongly.

In visualizers: Right now, projectM (with its Qt and SDL frontends) and Butterchurn (web) dominate usage. AVS is legacy/hobby only. A “competitor” could be something like Magic Music Visuals (commercial software for custom music visuals, node-based, not MilkDrop-related). Magic is powerful and used by some VJs, but it’s $40+ and not focused on the MilkDrop aesthetic. If a new tool combined MilkDrop’s library of presets with a friendly UI, it could undercut commercial tools for a segment of users who specifically love that retro look. Additionally, as VR and AR come up, music visualization might find new contexts (imagine an AR text rain or VR ANSI tunnel – speculative, but the tech could be repurposed).

Gaps/Opportunities Mapped to Desired Features

All-in-one Modern Text Art Suite: There is a clear opening for a cross-platform ANSI/ASCII editor that combines the best of all predecessors:

Full CP437 and Unicode support,

Advanced drawing tools (yes, brushes and shapes in a text context),

Multi-layer compositing with alpha (for complex ANSI overlays or blending ASCII with background images),

Animation timeline for ANSI (something only Durdraw attempted in terminals),

Integrated figlet/boxes for ASCII banners,

Collaboration (even if not heavily demanded, it could spur new community interactions like live multi-user art jams).

No current tool does all this. The market size might be small, but being the tool every ASCII/ANSI artist switches to is achievable by hitting these notes. Monetization could be via donations or a modest price on app stores (but given precedent, open-source is the more accepted route here).

Web Integration & Preservation: Offering web publishing (one-click upload to a gallery with proper credits and SAUCE preserved) could leverage the nostalgia on social media. Also, ensuring output works on modern terminals (e.g., testing art in Windows Terminal, VS Code, etc.) and providing an embeddable viewer (like a script tag that can render ANSI on a webpage accurately) could make the tool not just an editor but a platform for experiencing text art.

Revamped Visualizer Authoring: For Winamp-style visualizations, the creative community has dwindled partly because the tools to create presets remained arcane. A modern UI (maybe node-based like AVS but using modern shader building blocks) could attract both old preset authors and newbies who are intimidated by code. This tool could coexist with the editors or be a mode within a larger creative app. An example concept: a unified “Demoscene Lab” where one can draw ASCII art and craft music visualizers, since both are demoscene-adjacent arts. This is an ambitious merge of domains, but it could set a product apart.

If not combined, at least learning from each when designing: e.g., shader visualizer could borrow timeline ideas from animation editors; ASCII editor could borrow audio-reactivity for fun (why not allow animating ANSI art to music? Some BBS intros did scroll text to music beats).

Given MilkDrop presets are now basically GLSL shaders, tapping into the vibrant Shadertoy community is an opportunity: maybe allow import of simple Shadertoy shaders or provide a library of common visual effects so users can “tweak a preset” with sliders instead of coding. There’s definitely interest – people still share new MilkDrop presets in the Winamp forum up to 2020s, and projects like the MilkDrop Neural Network (HuggingFace) hint at a desire to automate or simplify preset creation.

Mobile & Tablet Experiences: No major ASCII art editor exists on Android/iPad (except some barebones apps). Tablet with pencil could be awesome for drawing text art (hand-drawn ANSI? might be neat). On the visualization side, phones and tablets are powerful enough to do these effects (projectM is on Android). A good touch UI for either drawing ASCII or performing visuals live (touch VJ controls) could open a new user segment (e.g., hobbyist VJs, or just bored commuters making ASCII doodles). If resource and scope allow, having a mobile companion app – even read-only (viewer) or simple editor – enhances the ecosystem.

Competitive Highlights

Strengths of incumbents:

PabloDraw: rock-solid, widely compatible, multi-user sync – but stagnated in features.

Moebius: cutting-edge features (half-block, cross-platform, open) – but not 1.0 yet, no animations or collab.

Icy Draw: new and actively soliciting features – could evolve fast; currently has momentum.

projectM/Butterchurn: have solved cross-platform playback – any new preset tool can build on their playback engines rather than reinventing.

AVS (old) and others: tons of legacy content to leverage (if you can support/import it, you instantly have a library of effects for users to study or remix).

Weaknesses/gaps:

Many tools have poor UI/UX by modern standards (e.g., steep learning curve, or terminal UI). This scares off newcomers who might otherwise dabble in ANSI art. A modern app with a friendly UI (tooltips, modern design conventions) could win adoption from curious new users who stumble on ANSI art.

Lack of documentation is common in open-source projects; a project that provides good docs, tutorials, and maybe community plugins (think an extension system for new effects or formats) would stand out.

Uniqueness & Ecosystem Leverage:

If the new tool can leverage existing ecosystems – e.g., allow plugging in FIGlet fonts, TheDraw .TDF fonts, ImGUI for scripting GUI, Shadertoy importer – it gains functionality by standing on shoulders of giants.

Integration with Mystic BBS or other modern BBS software: Mystic BBS (a modern BBS package) has a built-in editor; maybe a modern external editor could interface directly with a BBS to upload screens or allow "live editing" of a BBS menu. That would be novel.

Possibly connect ASCII art with the NFT/art blockchain trend (there was a brief fad of generative text art NFTs). While speculative, supporting outputs like SVG (vector text art) could allow people to print high-res posters of their ANSI art or sell them as digital collectibles. (There was an instance of an ANSI art piece sold as NFT by an artist, if memory serves.)

Overall, the market brief identifies that while these domains are somewhat retro-niche, they are experiencing a renaissance powered by nostalgia and new technology (web, open source, demoscene events). A well-crafted modern tool, if properly communicated, could become the go-to platform in these circles. The key is to respect the rich legacy (support old formats, honor the culture of attribution and community) while injecting fresh ideas and convenience that today’s users expect.

Ranked Feature Wishlist (MVP → V1 → V2)

Finally, based on the research, here is a prioritized wishlist of features for a hypothetical modern cross-platform text-mode art and visualization editor. The features are ranked by a combination of user demand (as evidenced by community discussions), uniqueness (how much it sets the tool apart), development effort (feasibility), and how well it leverages existing ecosystems:

MVP (Minimum Viable Product) – Core essentials to satisfy basic needs:

Core ANSI/ASCII Editing Tools: A robust drawing interface with resizable brush (single char and “stamp” modes), color palette picker, line/rectangle/ellipse tools, fill tool. These are table stakes – virtually all artists expect them (PabloDraw, Moebius have these) and lack of these is a non-starter.

CP437 and Unicode Support: Ability to switch between classic 256-character mode and a Unicode mode. As user XaviousD put it, “Unicode glyphs” and “256 color XTerm” support open new possibilities
reddit.com
. This is high demand especially for new-school artists who want to use block elements, braille patterns, or mix scripts. (Evidence: Reddit comments listing Unicode as #1 feature
reddit.com
; Durdraw and MoebiusXBIN making it a priority.)

Multi-platform Release: From day one, have builds for Windows, macOS, and Linux. The community is diverse and being inclusive gains goodwill. Tools like Moebius and Icy Draw earned praise by being cross-platform out of the gate
reddit.com
. Use a cross-platform framework (Qt, Electron, .NET MAUI, etc.).

Import/Export Formats: ANS, PNG, and SAUCE support are critical. The tool must read/write ANSI (.ANS) with SAUCE without data loss (or people will avoid it)
github.com
. PNG export (for sharing on web easily) should be built-in (leveraging something like Ansilove library internally to ensure accuracy
github.com
). Export to plain TXT and HTML (for ASCII art) also high value. (Evidence: Every modern tool touts its export options, and users often ask “can it export to PNG?” on forums – e.g., Durdraw instructs installing Ansilove for PNG export
github.com
.)

Undo/Redo & Auto-save: A deep undo stack (not just one-level like TheDraw) is expected now. Autosave or recovery is also important – losing hours of art to a crash is painful (older tools were not always stable). Modern UX expectations.

Basic UI Modernity: Things like zoom (people want to zoom in to do pixel-precise placements) – e.g., RexPaint scales by changing font size on the fly
curlie.org
. Smooth panning, grid toggles, perhaps optional guidelines for text baseline or centering. These might seem minor, but they drastically improve usability and match modern design tool feel.

(MVP rationale: These features ensure the tool is actually usable and not missing fundamentals that every other tool has. If any of these were missing, it would be hard to get users to switch.)

V1 (First full version) – The standout features that address unmet needs:

Layers and Blending: Implement multiple layers of text with blending modes (at least simple alpha or additive). Demand: High – artists have long wanted to compose complex scenes in parts (one Redditor explicitly listed “5: Layers” as something they want to see in editors
reddit.com
). RexPaint’s popularity in part comes from its multi-layer ability
curlie.org
. Layers would be relatively unique in ANSI art (only RexPaint and Icy Draw have it in some form).

Selections & Transformations: Advanced selection tools – not just rectangular, but lasso or flood (magic wand by color) selection if possible, and the ability to move, rotate (90-degree steps at least), flip horizontally/vertically the selected region. Evidence: Users mentioned using two instances of editors to copy/paste between files as a workaround
reddit.com
 – a single app that lets you copy-paste across canvases or files would save time. Transformation requests come up as well (even if rotation in text can be lossy except 90°, it’s useful for box-drawing art).

Integrated FIGlet/Fonts and Text Generators: Include a library of fonts (TheDraw’s .TDF fonts, FIGlet fonts, etc.) and a tool to type a string and insert an ASCII art banner. Demand: Implied by how almost every artist at some point uses FIGlet or TheDraw’s font feature for titles. Icy Draw’s dev was asked to include TheDraw fonts
youtube.com
. Having this built-in would draw users who currently rely on external tools and then import.

Pattern Brushes / Stamps: Ability to select an area (e.g., a 2x2 or 3x3 block of characters) and use it as a repeating brush. Great for drawing borders, textures, etc. Evidence: Historically, artists create “blocks” manually or copy-paste repeatedly. Moebius’s half-block brush is a form of this
blocktronics.github.io
. This feature increases efficiency for common patterns (like checkerboard, shading blocks). There’s clear value, though not widely advertised by users (because many don’t imagine it yet).

256-color / Truecolor mode: For Unicode/UTF-8 art, allow use of 256-color extended ANSI or even truecolor (24-bit) in text (supported by modern terminals). This intersects with “demoscene new school” where ASCII can have many colors (e.g., Blinkenshell ASCII with extended palette). Durdraw shows there is interest in 256-color text art
github.com
. It’s a unique selling point, even if not everyone uses it, it future-proofs the tool.

Extend to PETSCII/Teletext Modes: Possibly as modes or plugins – allow switching canvas to PETSCII character set or Teletext (size 40x25 with constrained color rules). This taps into those sub-communities. E.g., Petmate is great but if your tool can do both ANSI and PETSCII by just switching mode, multi-talented artists will prefer one tool. Given open-source code exists to handle those (Petmate, edit.tf), integration or inspiration is feasible.

Embedded Media Export: For example, export an ANSI drawing as an HTML5 canvas animation or an SVG (with each character as a <text> element) – the latter is super useful for making high-resolution prints of ASCII art or scalable designs. Monodraw’s ability to export SVG is appreciated by diagrammers
news.ycombinator.com
, and ASCII artists have used hacks to get vector output for poster printing. Including this would be unique in the ANSI space.

Preset Visualization Editor (MilkDrop/AVS): Introduce a separate mode or companion app for visualizers. For v1, maybe start simple: a MilkDrop preset tweaker – GUI sliders to modify common variables (wave amplitude, colors, etc.) and a text editor with syntax highlighting for the preset equations. Over time, evolve this into a more visual node editor. This feature crosses into the second domain of the research. It’s a bigger project on its own, but even basic functionality (like a UI to browse a folder of presets, preview them with your music, and edit values) would delight the small but passionate audio-visualizer crowd. Demand: Niche but high among those who care – the absence of a good editor is often lamented in forums (e.g., “is there a better way to make MilkDrop presets?”). Given our combined app concept, this is a unique selling point (no other ASCII art tool has this; it’d stand out as a demoscene multi-tool).

(V1 rationale: These features set the tool apart from any existing single competitor. They directly address many “I wish I had” moments from users (layers, better font tools, extended colors) and leverage other ecosystems (fonts library, extended char sets). They would likely make the tool the most feature-rich in its class.)

V2 (Next versions / Stretch Goals) – Innovative or heavy-lift features:

Real-time Collaboration: Multi-user editing on the same canvas over internet (like Google Docs but for ANSI art). PabloDraw did this on a LAN/Direct IP basis
facebook.com
; doing it with modern networking (maybe using web tech or cloud) could revive the fun of group draws. It’s technically complex (synchronization, conflict resolution), hence slated for later. But it’s a unique feature that could attract people for the novelty and community events (collaborative art jams).

Plugin/Script System: Allow advanced users to extend the tool – e.g., a Python or Lua scripting console to manipulate the canvas (for procedural effects like “wave warping” the text, or automatically importing an image and dithering it). This taps creative coders and could lead to user-contributed plugins (much like GIMP or Photoshop have). Visualizer side: maybe allow plugins to add new waveform analyzers or effects.

Audio-Reactive ANSI Mode: Here’s a wild idea: merge the two domains – let the editor have an “audio reactive” mode where ANSI art can respond to music (as a visualization). For example, you could place some special markers or use certain characters that flip between two states on beat, etc. Essentially an ANSI demo maker. This would be totally novel – turning static text art into a simple music visualization. It could export as a series of ANSImation frames or a video. It leverages our visualizer code but applies it to text art. This could result in fun outputs (imagine an ASCII equalizer that jumps in your ANSI image). This is definitely a niche within a niche, but it would embody the demoscene spirit and generate buzz.

Android/iPad App Variant: Depending on tech stack, either a full port or a companion viewer. The reason it’s valuable: show your ANSI art on your phone, or sketch ideas on the go. For visualizers, an Android app is essentially already done by projectM for playback, but an editor on tablet for presets or text art (with pencil support on iPad for hand-drawn text strokes) could be groundbreaking. This has moderate demand; for instance, an artist might want to draw on a tablet with a stylus instead of mouse – currently impossible for ANSI art. It’s a lot of dev work though, hence V2.

JS/Web Embeddable Viewer Library: By V2, formalize the viewing side: a JavaScript library that can take an ANSI/ASCII file (with SAUCE) and render it exactly as the editor would, in a web canvas or DOM. This can be offered as a standalone library (like “TextArt.js”). It leverages internal rendering code. Demand is there – many sites roll their own (16colo.rs uses Ansilove web, etc.), but an officially supported viewer means any art shared can include a mini viewer ensuring it looks right. It also promotes the editor (free marketing, as art posted with that viewer could say “made with X”). Since the research specifically noted web rendering libs, providing one consolidates ecosystem around your tool.

Performance Benchmark: 100K characters and Beyond: Ensure that by V2 the app can handle extremely large artworks or animations (for instance, an ASCII art of size 1000x1000, or a loop of 200 frames) without crashing. This might involve optimizing data structures (maybe using tilemaps or GPU acceleration for rendering). It’s more of a technical goal than a feature, but it’s something that will allow new kinds of usage (like giant banner prints or long scrolling animations).

Integration with BBS/Network: Possibly a feature to connect to a live BBS to edit its menus online, or at least an uploader to BBS (via telnet/SSH) to test how your ANSI looks on an actual board. Since some BBSes still run (and new ones on telnet), this would delight sysops. Not mass-market, but it fits the ethos of catering deeply to the scene. (One user in the Reddit thread was asking about BBS-specific features like @ codes for user name insertion
reddit.com
 – our tool could include templates for major BBS software codes, making life easier for BBS modders.)

(V2 rationale: These are the “wow” features that could either push the envelope of what’s possible or integrate the tool deeply into workflows. They’re higher effort or more experimental, which is why they come later. They could also attract attention beyond the immediate community – e.g., collaborative ASCII art might get tech blog write-ups; audio-reactive ASCII might create a new micro-genre of art.)

Evidence & Demand Recap for Wishlist:

Layers & Unicode (V1) – explicitly requested by multiple community members
reddit.com
reddit.com
; proven useful in RexPaint, Icy Draw.

Brushes & Patterns (MVP/V1) – Moebius’s success with half-block brush
blocktronics.github.io
 shows innovative brush tech is appreciated. Figlet inclusion frequently comes up in tool discussions.

Collaboration (V2) – PabloDraw’s enduring use for network sessions indicates some continued interest, though it’s niche. It’s the kind of feature that isn’t demanded loudly but when available could spark new usage (surprise-and-delight).

Web integration (V2) – The research noted multiple ANSI-to-web projects, meaning developers have spent effort here. A unified solution from the editor side would meet a known need.

Audio visualization editing (V1/V2) – While not a mass request (because few imagine it possible beyond Winamp), the enduring MilkDrop preset community and projects like new preset packs and Butterchurn show the content still has value. A user-friendly creation tool is the logical next step; given no one else has done it, even moderate demand is unmet.

In conclusion, the roadmap prioritizes getting the basics perfect (so the existing user base can comfortably migrate to the new tool), then introducing the most asked-for enhancements (layers, Unicode, extended colors), and finally innovating in ways that merge the ASCII art and visualization domains or otherwise leverage modern tech (collab, scripting, AR/VR possibly). By following this wishlist, the resulting product would not only cover the current market gaps identified (lack of a one-stop modern editor, and lack of a modern preset editor) but also push the boundaries of what’s considered text-mode art and visualization, potentially growing the market by inspiring new creative use-cases.

Tech Stack Options for an ASCII/ANSI Art Editor
Developing an ASCII/ANSI art editor with a custom UI/UX (targeting Linux desktop first, with potential web deployment) can be approached in multiple ways. Below we outline recommendations in Rust, Python, and other stacks, along with suitable frameworks for each:
Option A: Rust for a Native & Web-Capable Editor
Rust offers high performance and a single-binary deployment, which is great for a desktop app on Linux. Modern Rust GUI libraries also support cross-platform development and even web compilation (via WebAssembly):
Iced (Rust) – A cross-platform GUI library for Rust focused on simplicity and type-safety (inspired by Elm)
github.com
. Iced can deliver a native desktop UI and is suitable for custom drawing (you could create a widget to render your text canvas). Its architecture (Elm-like update/view) helps in managing state cleanly.
egui + eframe (Rust) – An easy-to-use immediate-mode GUI library in Rust. egui is simple, fast, and runs both natively and on the web (via WASM)
github.com
github.com
. Using the official eframe framework, you can write an app once and deploy it to Linux, Windows, Mac, and even compile to WebAssembly for a browser-based version
github.com
. This could cover your “desktop first, but web-based explored” requirement with one tech stack. Immediate mode GUI is very flexible for custom drawing (e.g. rendering an ANSI text grid via textured triangles).
Terminal UI (TUI) in Rust – If you’re open to a text-mode interface for the editor, Rust has libraries like crossterm or higher-level frameworks like tui-rs (ratatui). These allow building an interactive terminal UI with ANSI colors and mouse support. This fits the ASCII art theme and keeps it lightweight in a Linux terminal, though designing a mouse-friendly UI in a terminal is more limited than a GUI.
Rust + Web (Hybrid) – You could also consider a hybrid approach using web technologies for the UI with a Rust backend. For example, Tauri uses a Rust backend (compiled to a native binary) and a frontend rendered in a system WebView
gethopp.app
gethopp.app
. This yields a much smaller app bundle than Electron by not shipping a full browser
gethopp.app
. Tauri lets you write the UI in HTML/JS (or any web framework) but keeps resource usage low (e.g. memory and bundle size are a fraction of Electron’s)
gethopp.app
. If you prefer pure Rust, frameworks like Yew or Dioxus let you create a web-based UI in Rust (WASM) as well.
Why Rust? It gives you speed and control – useful if you later integrate real-time features like audio visualization. You get a native Linux app with efficient use of resources, and the option to target web via WASM without rewriting your core logic. The trade-off is that Rust GUI ecosystem is younger than, say, Qt or web frameworks, so you might invest time in the GUI development. However, libraries like Iced and egui are quite developer-friendly (inspired by Elm and ImGui patterns respectively) and have active communities.
Option B: Python for Rapid Development
Python can speed up development and has multiple frameworks for building both graphical and text-based UIs. This is great for quickly prototyping your editor’s features, though you may need to manage performance for very large images or real-time updates. Some Python options:
PyQt / PySide (Qt for Python) – PyQt5/PyQt6 or PySide6 are Python bindings to the Qt framework. Qt is a mature C++ GUI toolkit that is cross-platform (Linux, Windows, Mac) and supports native look-and-feel
dev.to
. Using PyQt, you can create a robust, highly functional GUI relatively easily
dev.to
. This would let you design a custom interface (Qt’s canvas and painting system could render your ANSI canvas, or even use a QTable-like grid of colored text). The benefit is a professional UI toolkit with tons of features (menus, dialogs, etc.) ready-made. The downside is the deployment – your users would need Qt libs (you can bundle them using tools like PyInstaller or cx_Freeze).
Kivy – An open-source Python framework specifically for building custom UI/UX applications with graphics acceleration. Kivy is cross-platform (Linux, Windows, Mac, Android, iOS) and is designed for highly custom interfaces (it even supports multitouch)
kivy.org
kivy.org
. For an ASCII art editor, Kivy would allow you to draw the text grid as sprites or textures on a Canvas, giving you full control over how it looks and interacts. Kivy apps don’t use native widgets, so your UI can be completely bespoke (which fits “fully custom UI/UX”). It’s also suitable if you think about adding animations or transitions in the editor.
Textual (Textualize) – If you’re open to a terminal-based UI implemented in Python, Textual is a modern TUI framework that brings web-like layout and styling to the terminal. It allows building sophisticated text-mode interfaces with a simple Python API
textual.textualize.io
. Notably, Textual apps can run in the terminal and (in the future/currently via their platform) in a web browser as well
textual.textualize.io
. This could be an interesting way to create an ASCII art editor that runs in a terminal (over SSH, etc.) while still supporting mouse, colors, and even potentially a web view. It’s built on Rich, so it supports rich text and color rendering in terminals. This option keeps the “spirit” of ASCII art by using an actual text console for editing, but you’d have to implement a lot of editing mechanics (mouse interactions, region selection, etc.) within Textual’s framework.
Other Python Tools – If not using the above, more minimal routes include Python’s built-in curses (for a simple terminal editor interface) or libraries like Pygame/Pyglet for a DIY GUI (drawing text to a window manually). These give you control but require more work. For example, using Pygame you could blit a bitmap font to simulate text mode. However, given your requirements, a higher-level framework like Qt or Kivy will get you productive faster.
Why Python? It excels in rapid development and has a gentle learning curve for UI work (especially with Qt designer or Kivy’s KV language). If you anticipate a lot of iteration on the editor’s features or are more comfortable in Python, this route gets you results faster. Just plan for distribution (bundling a Python app can be trickier than a Rust binary) and be mindful of performance if the editor manages very large text buffers or needs real-time responsiveness (you might need to use numpy or C extensions if heavy processing is involved).
Option C: Other Tech Stacks (C++ or Web Technologies)
Considering you are open to C++ and JavaScript as well, it’s worth noting a few other paths:
C++ with Qt or similar – This is the traditional route for cross-platform GUI applications. Using C++ with the Qt framework would give you maximum performance and native UI on Linux/Windows/macOS. Qt is a comprehensive toolkit (everything from GUI to audio, networking, etc.) and produces highly optimized native code
qt.io
. You could leverage Qt’s text rendering to implement the ANSI art canvas and use Qt’s model-view features for things like color palettes, layers, etc. The learning curve is steeper (and development slower) compared to Python, but you get full control. Another C++ option is Dear ImGui (immediate-mode GUI library) which can be useful if you embed your editor in a rendering loop (commonly used in game tools). There are also lighter GUIs like FLTK or SDL if you prefer simpler frameworks. Overall, C++ is a solid choice if you want to follow the footsteps of older editors (many DOS-era editors were in C/C++, and the modern cross-platform PabloDraw uses a C# (Mono) approach similar to C++). For instance, PabloDraw adopted the Eto.Forms .NET framework to achieve native UIs on all OSes
goodfirms.co
 – showing that performance-critical parts can be handled in C/C++ (or .NET) while getting a cross-platform UI.
Web App (HTML5/JS) – Building the editor as a web application can be attractive for a rich, easily-accessible UI. You’d create the interface using web technologies (HTML/CSS for layout, Canvas or WebGL for drawing the text grid, JavaScript/TypeScript for logic). This makes it simple to run on any platform (just open in a browser), and you could later wrap it in an Electron shell or similar for desktop distribution. In fact, the Moebius ANSI editor is a recent project that uses web tech – it runs as a desktop app but is built with an Electron/Web stack (providing cross-platform support on Linux, Windows, Mac)
blocktronics.github.io
. The advantage is you can leverage existing libraries (for example, any JS library for color pickers, etc.) and web development tools. However, pure Electron apps tend to be heavy on resources (since you’re essentially running a Chromium instance). The alternative Tauri, as mentioned, can mitigate some of this by using system webviews and Rust for backend – but either way, a web UI will use more memory than a native UI. If you go this route, you could also consider a progressive web app approach (for the browser) and only use Electron/Tauri if a desktop installation is needed. Given that audio visualization might be a future component, note that the Web platform has WebAudio and Canvas which could handle that as well, albeit not as performance-efficient as native code.
Hybrid or Other – There are other stacks like Flutter (Dart) which can build desktop and web apps with one codebase, or Java (with JavaFX or Swing) for desktop, but these might be less ideal given your openness to C++/JS and the mentioned options. If you want a single framework that can target desktop and web, you might look at something like Slint – a declarative UI framework that supports Rust, C++, JavaScript, and even Python for the logic layer
slint.dev
. Slint allows designing the UI in a markup language and integrating with logic in the language of your choice, compiling to native code. This is a more niche solution, but it shows how multiple language support could be possible in one project.
Summary & Recommendation
Each approach has its merits. Rust would give you a lean, high-performance native app (with an easier path to WebAssembly if you want a browser version of your editor). It’s a great choice if you value efficiency and plan to possibly integrate lower-level audio/graphics processing. If you do choose Rust, libraries like Iced
github.com
 or egui
github.com
 are strong candidates for building a custom UI from scratch. On the other hand, Python lets you get something working quickly. With frameworks like PyQt (leveraging Qt’s power)
dev.to
dev.to
 or Kivy
kivy.org
, you can craft a fully custom interface and iterate faster; just be prepared to optimize or move parts to native code if performance becomes an issue. And if neither of those feels right, a C++/Qt solution remains a reliable (if more labor-intensive) route for a polished cross-platform app, while a Web-based solution (JS/TS) could shine if you want maximum portability and a rich UI, at the cost of higher resource usage (Electron) unless using a hybrid like Tauri
gethopp.app
. In practice, many modern ANSI art editors have embraced cross-platform stacks: for example, PabloDraw used .NET with Eto.Forms for native UIs
goodfirms.co
, and Moebius uses an Electron web app approach
blocktronics.github.io
. Given your criteria, my suggestion would be to prototype quickly in Python (to flesh out the features and UI design), but consider moving to Rust (or C++) for the implementation if you need the performance and a long-term lighter-weight solution. If you’re comfortable with web development, you could also prototype the UI in a browser (easy testing and iteration) and then later wrap it with a Rust backend via Tauri for a more efficient desktop app. Ultimately, the “best” tech stack depends on your familiarity and the importance of factors like development speed vs. runtime performance. Any of the above can achieve a Linux-first ASCII/ANSI editor with a custom UI – it’s about what trade-offs you’re most willing to make. With modern frameworks, both Rust and Python ecosystems can deliver what you need:
For fastest results: Python with Qt/Kivy will get a working editor up quickly.
For best performance and longevity: Rust or C++ with a native GUI toolkit will yield a snappier, leaner app (and still cross-platform).
For broad accessibility: Web tech (JS/HTML5) ensures anyone can run it in a browser, and you can still package it for desktop later.
Consider trying a small proof-of-concept in one or two of these stacks to see which aligns with your development style and requirements. Good luck with your ASCII/ANSI art editor project! Sources:
Rust Iced GUI library – “iced is a cross-platform GUI library for Rust focused on simplicity and type-safety inspired by Elm.”
github.com
Rust egui library – “egui... is a simple, fast, and highly portable immediate mode GUI library for Rust. egui runs on the web, natively, and in your favorite game engine.”
github.com
egui’s eframe (multi-platform support) – “eframe is the official egui framework, which supports writing apps for Web, Linux, Mac, Windows, and Android.”
github.com
Textual (Python TUI) framework – “Build sophisticated user interfaces with a simple Python API. Run your apps in the terminal or a web browser!”
textual.textualize.io
PyQt (Qt for Python) overview – “PyQt is a set of Python bindings for the Qt toolkit... It supports Windows, Mac OS and Linux... allows Python programmers to create programs with a robust, highly functional GUI, simply and easily.”
dev.to
dev.to
Kivy framework homepage – “Build and distribute beautiful Python cross-platform GUI apps with ease. Kivy runs on Android, iOS, Linux, macOS and Windows... built to be easy to use, cross-platform and fast.”
kivy.org
kivy.org
PabloDraw cross-platform approach – “PabloDraw... uses the awesome Eto.Forms cross-platform framework to provide native UI for Windows, OS X, and Linux.”
goodfirms.co
Moebius ANSI Editor info – “Moebius is a new ANSI and ASCII Editor for MacOS, Windows, and Linux... (half-block brush feature, etc.)”
blocktronics.github.io
Tauri vs Electron resource usage – Comparison: Tauri (Rust + WebView) vs Electron (Chrome) – e.g., bundle size ~8.6 MiB vs 244 MiB, memory 172 MB vs 409 MB in a sample app
gethopp.app
. This highlights the efficiency of a Rust+WebView approach.
Citations
￼
GitHub - iced-rs/awesome-iced: A curated list of custom widgets, example projects, integrations, and resources made with/for iced

https://github.com/iced-rs/awesome-iced
￼
GitHub - emilk/egui: egui: an easy-to-use immediate mode GUI in Rust that runs on both web and native

https://github.com/emilk/egui
￼
GitHub - emilk/egui: egui: an easy-to-use immediate mode GUI in Rust that runs on both web and native

https://github.com/emilk/egui
￼
Tauri vs. Electron: performance, bundle size, and the real trade-offs

https://www.gethopp.app/blog/tauri-vs-electron
￼
Tauri vs. Electron: performance, bundle size, and the real trade-offs

https://www.gethopp.app/blog/tauri-vs-electron
￼
Tauri vs. Electron: performance, bundle size, and the real trade-offs

https://www.gethopp.app/blog/tauri-vs-electron
￼
PyQt: cross-platform GUI programming - DEV Community

https://dev.to/jones268/pyqt-cross-platform-gui-programming-ba9
￼
PyQt: cross-platform GUI programming - DEV Community

https://dev.to/jones268/pyqt-cross-platform-gui-programming-ba9
￼
Kivy: Cross-platform Python Framework for GUI apps Development

https://kivy.org/
￼
Kivy: Cross-platform Python Framework for GUI apps Development

https://kivy.org/
￼
Textual

https://textual.textualize.io/
￼
Textual

https://textual.textualize.io/
￼
Qt | Development Framework for Cross-platform Applications

https://www.qt.io/product/framework
￼
PabloDraw Reviews & Pricing 2025

https://www.goodfirms.co/software/pablodraw
Moebius ANSI Art Editor

https://blocktronics.github.io/moebius/
￼
Slint | Declarative GUI for Rust, C++, JavaScript & Python

https://slint.dev/
￼
PyQt: cross-platform GUI programming - DEV Community

https://dev.to/jones268/pyqt-cross-platform-gui-programming-ba9
All Sources
￼
github
￼
gethopp
￼
dev
￼
kivy
￼
textual.textualize
