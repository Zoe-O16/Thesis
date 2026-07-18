# RollingLDA Topic Codebook


## Coding instructions

Each fashion runway review is classified into exactly one of ten predefined topics, numbered 0–9, using the accompanying codebook. The decision rests only on what the review itself says, setting aside any external knowledge of particular designers, brands, or fashion history not stated in the review.  When a review appears to fit two topics, the exclusion criteria in the codebook are consulted: each topic lists the topics it is most easily confused with, and these criteria are checked directly against the review text to break the tie.

---

### Topic 0: Masculine-inflected tailoring and leather

**Description:** This topic covers reviews centered on structured, tailored garments, such as blazers, trousers, and sharp-shouldered jackets, described with an emphasis on masculine, androgynous, or gender-crossing elements. The tailoring is the organizing subject of the review. If leather is mentioned, it functions as a tailoring material (e.g., a leather jacket or trouser) rather than as an accessory or outerwear material.

**Inclusion criteria:**

Reviews where the primary subject is structured tailoring (blazers, trousers, sharp shoulders), including cases where the structure is conveyed through language like "strong shoulders," or "sharp lines" rather than a garment list; Reviews where the collection or pieces are described using masculine, androgynous, or gender-blurring language, including casual phrasing such as "boyfriend", not only explicit words like "masculine"; Reviews where leather appears as part of the garments as a defining material.

**Exclusion criteria:**

Reviews centering on fur or luxury outerwear rather than tailored separates, even if some structured pieces are mentioned (see Topic 3); Leather appears mainly in an accessories context (bags, belts), or a single garment is described as leather with no repetition and no structured-silhouette language around it; Reviews where masculine or androgynous language appears early on but the review's own closing assessment is about everyday, practical wearability rather than the gender-blurring point (see Topic 9).

---

### Topic 1: Glamour, eveningwear, and occasion dressing

**Description:** This topic covers reviews of formal eveningwear, such as gowns and cocktail dresses, discussed how they are constructed: silhouette (column, A-line), neckline, beading, draping, and fabric (silk, chiffon, satin). The review focuses on the garment, specifically how it is built and how it moves. 

**Inclusion criteria:**

Reviews focused on gown or cocktail dress construction (silhouette, neckline, beading, draping); Reviews describing formal eveningwear primarily through fabrication and construction detail; Reviews where the bulk of the description is devoted to the garments that fit the previous criteria; Reviews of otherwise mixed-category collections that single out gowns or cocktail dresses as the strongest pieces described through construction detail, even if sportswear, denim, or separates dominate the earlier part of the review.

**Exclusion criteria:**

Reviews where red-carpet spectacle and the glamour of the event rather than the clothing carries the bulk of the review's attention (see Topic 5); Reviews where lace, corsetry, bra-tops, or a lingerie-derived sensuality is the main focus of the eveningwear rather than gowns (see Topic 6); Reviews of career-retrospective or anniversary shows where the gowns are discussed as artifacts of a designer's history rather than as the focus of the current show (see Topic 4).

---

### Topic 2: Graphic print and nightlife dressing

**Description:** This topic covers reviews of print- and pattern-driven casual clothing, along with disco, party, or nightlife-coded garments, or reviews where pattern and graphic print are explicitly named as the collection's main visual subject regardless of mood. The print or graphic pattern, is where the review's attention lies.

**Inclusion criteria:**

Reviews built around a print- or pattern-led casual garment or collection (denim, jean pieces, graphic prints, novelty patterns); Reviews describing a disco, party, retro-decade, or nightlife-coded aesthetic; Reviews where pattern and graphic print, rather than cut or fabrication, is the main visual subject even without a disco/party/nightlife addition.

**Exclusion criteria:**

Reviews fitting any other categories where print makes an incidental appearance;  Reviews where casualwear centers more around youth, sport, or athleisure-specific narrative (tracksuits, activewear, logos) rather than a print-led nightlife aesthetic (see Topic 7); Reviews where casualwear centers more around utlity and urban aesthetics (see Topic 9); Reviews built around a soft, pale, floral print rather than a bold, graphic, party-coded one (see Topic 8); Reviews where bra-tops, lace, or corsetry are also named, even just once or twice, alongside the print (see Topic 6) as a specific lingerie-derived garment is a stronger signal than a generic print description.

---

### Topic 3: Luxury fabrics, furs, and outerwear

**Description:** This topic covers reviews of seasonal outerwear, such as coats, made of heavier, luxury materials such as fur, shearling, and mink. The topic applies whenever this vocabulary is the most emphasized in the review, or if garments fitting this description are flagged by the review itself as the standout or best piece.

**Inclusion criteria:**

Reviews focused on a fur or outerwear garment (coat, shearling, mink, sheepskin); Reviews where a luxury fabric (cashmere, shearling, mink, camel hair, tweed, tartan) defines the collection's identity; Reviews describing seasonal Fall/Winter outerwear as a category in its own right; Reviews of mixed-theme Fall collections (staged, print-led, or concept-driven) where fur, shearling, or coats are named repeatedly, or singled out by the review as the strongest pieces.

**Exclusion criteria:**

Reviews where leather appears as a tailoring material within a structured, gender-inflected silhouette, and it is the silhouette itself, not the fur or leather as a material, that the review dwells on (see Topic 0); Reviews where a coat or jacket is discussed only for its practical, everyday layering function, with no luxury-fabric language and no repetition (see Topic 9); Reviews where fur or outerwear is mentioned exactly once in passing, within a collection whose main subject is something else.

---

### Topic 4: Designer vision, technical mastery, and intellectual authority

**Description:** This topic covers reviews that evaluate a designer's conceptual, intellectual, or technical skills and ambitions, rather than describing individual garments in detail. The review reads as criticism of the designer's ideas and execution as a body of work, often invoking art history, architecture, or the designer's broader career trajectory. This topic applies only when the designer is the review's sole focus. If the collection's garments are described in more detail than the designer elsewhere in the review (specific fabrics, silhouettes, decorative details), classify by that garment vocabulary instead, even if the review opens with or repeatedly returns to the designer's stated inspiration.

**Inclusion criteria:**

Reviews centered on critical evaluation of a designer's concept, artistic or architectural references, or intellectual ambition, where no other topic's garment vocabulary (fur/coat, gown construction, lace/bra-tops, tailoring, print, sport/denim, pastel/pretty mood, separates) is present in force; Reviews that assess a designer's technical skill, innovation, or authority as the main point of the piece (e.g., fabric science, garment construction technique, sustainability process) rather than the garments' category; Reviews discussing a designer's career-long vision or retrospective body of work (e.g. an anniversary), where garments are explicitly framed as artifacts of that career narrative rather than described in their own right.

**Exclusion criteria:**

Reviews describing the cut and construction of specific garments rather than the designer's conceptual stance (see Topic 0); Reviews where a show's staging, venue, or performance elements, rather than the designer's ideas, are what the review dwells on (see Topic 5); Reviews that name a designer's vision or inspiration in the opening lines but otherwise focus on describing individual garments matching another topic's vocabulary, classify by that garment vocabulary instead; Reviews organized around a single named seasonal concept or theme-title for this particular show, as opposed to the designer's career more broadly (see Topic 5).

---

### Topic 5: Conceptual staging and theatrical collection

**Description:** This topic covers reviews built around a show's staging, performance, or conceptual premise. This may include an unusual venue, live performers, a theatrical set piece, or a single named thematic idea governing the whole show, as the primary thing the critic responds to.

**Inclusion criteria:**

Reviews centered on the staging, presentation format, or performance concept of a show (venue, set design, live performance elements, props); Reviews where a show's spectacle or premise dominates the review, with garments described mainly in service of that concept; Reviews of shows explicitly framed as performance art, theater, or an immersive experience; Reviews organized around a single named seasonal theme or title (e.g., a one-word concept, an archetype, a titled show), even without a physical set, as long as no other topic's garment vocabulary dominates instead.

**Exclusion criteria:**

Reviews where formal eveningwear construction, rather than the staging or performance, is what the review dwells on, even if a dramatic setting is named (see Topic 1); Reviews that evaluate the designer's intellectual or artistic vision as a career-long or retrospective body of work, independent of a specific staged event for this season (see Topic 4); Reviews where garment characteristics, are emphasized more independently of the concept of the show.

---

### Topic 6: Lace, lingerie, and sensuality

**Description:** This topic covers reviews built around a lace- and lingerie-derived decorative vocabulary, such as corsetry, bra-tops, ribbon detailing, satin, and sheer fabrication, marking a sensual aesthetic, or reviews invoking mythic or goddess-coded sensuality. The review's attention centers on the erotic, intimate, or mythic charge of the collection.

**Inclusion criteria:**

Reviews centered on lace, lingerie-inspired construction, corsetry, or bra-tops as the defining characteristics of the garments, even if mentioned only once or twice; Reviews describing a sheer, sensual, or decoratively intimate register (bra tops, slip dresses, exposed boning); Reviews invoking a mythic, "goddess," or old-Hollywood sensuality, whether or not lace or lingerie detailing is also present.

**Exclusion criteria:**

Reviews centered on formal gown construction (silhouette, neckline, beading) where lace or lingerie detailing is absent or incidental (see Topic 1); Reviews where the register is described only in soft, pale, or romantic mood words ("boudoir," "soft," "romance") with no actual lace, corset, or bra-top garment named: a mood word is not the same as a garment (see Topic 8).

---

### Topic 7: Sportswear, denim, and youth casualwear

**Description:** This topic covers reviews of youth-coded, sport- or street-inflected dressing, such as denim, tracksuits, or activewear, where an association with youth culture, sport, or street style defines the collection. The tone tends to be upbeat and casual, often invoking a specific youth subculture (beach, skate, gym, festival).

**Inclusion criteria:**

Reviews centered on youthful, sporty, or street-casual dressing (denim, jean pieces, sneakers, sweatshirts, tracksuits); Reviews where tracksuits, activewear, or athleisure pieces define the collection's identity, or where such pieces are introduced as a notable "first" or departure for the brand; Reviews explicitly invoking a youth subculture or age-coded casual setting (teen, beach, skate, festival).

**Exclusion criteria:**

Reviews built around print- or pattern-led nightlife/disco dressing without a youth-sport or street angle (see Topic 2); Reviews built around practical, separates-led wearability aimed at a mature or professional wardrobe rather than youth culture (see Topic 9); Reviews where a single celebrity or news event, rather than a genuine youth/sport aesthetic, happens to dominate an otherwise unrelated show;

---

### Topic 8: Feminine spring lightness and romantic delicacy

**Description:** This topic covers reviews of a pale, floral, or generally light and pretty feminine aesthetic, described through soft, delicate, whimsical, or romantic language, such as broderie anglaise, crochet, sundresses, and pastel palettes. The mood is light and delicate rather than sensual, formal, or graphic, often invoking innocence, prettiness, whimsy, or a "girl" archetype.

**Inclusion criteria:**

Reviews centered on soft, pale, or floral dressing (sundresses, broderie anglaise, crochet, eyelet); Reviews describing a romantic, delicate, whimsical, or innocent "pretty" aesthetic, including Fall collections if the palette or mood is explicitly pastel, light, or dreamy; Reviews explicitly invoking a pale color palette (dusty, sherbet, sugar-almond, powder) or lightness as the collection's organizing aesthetic anchor point; Reviews using "soft," "romance," or "boudoir"-adjacent language, provided no actual lace, corset, or bra-top garment is also present.

**Exclusion criteria:**

Reviews where lingerie and sensuality dominate the review over mentions of softness or romance (see Topic 6); Reviews centered on formal gown construction (beading, column silhouettes, see Topic 1); 

---

### Topic 9: Utilitarian separates and wearability

**Description:** This topic covers reviews of separates-based dressing, such as jackets, pants, skirts, and coats, discussed through practical, utilitarian, and urban language. The review's attention centers on the separate pieces themselves and their everyday wearability, including cases where the review's own conclusion frames the collection as practical, wearable, or "for a well-dressed woman to throw on," even if other vocabulary (androgynous framing, leather) appears earlier.

**Inclusion criteria:**

Reviews centered on separates-based dressing (jacket, pant, skirt, coat) as the main subject; Reviews describing utilitarian or urban language applied to separates; Reviews framing a collection around wearability or practicality rather than spectacle, luxury status, or concepts; Reviews emphasizing practicality and everyday dressing.

**Exclusion criteria:**

Reviews where fur or seasonal luxury outerwear is named repeatedly or flagged as the standout piece, rather than a coat being discussed function (see Topic 3); Reviews where tailoring carries an explicit masculine or gender-blurring charge as the review's sustained point, not just an incidental phrase (see Topic 0); Reviews where separates are styled specifically for a youth or street-casual audience, or introduce denim/sneakers as a notable choice, rather than general practical wearability (see Topic 7).
