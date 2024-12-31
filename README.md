java c
CEGE0009 
Structural assessment of an existing building using GSA 
Coursework Brief 
Learning objectives: 
1.          To be able   to   model   frames   with   GSA
2.          Understand how a   reinforced concrete frame   is typically   modelled with   Finite   Elements   (FE)
3.          Understand   how   a   FE   global   structural   model   is   used   to   obtain   design   forces   of   particular   members and check against   their   resistance
4.          Practise capacity calculations of RC   members   and   execute   basic   code   checks
5.          Ability to validate an   FE model through   independent checks
6.          Ability to calculate the carbon savings from reuse
7.          Know how to   behave   professionally and ethically   as   part   of   a team
8.          Ability to write and draw   professionally paying   due   regard to   a target   audience
Assignment administration 
Total weight: 20% of   CEGE0009 module   mark
Group formation: This   assignment   in to   be   performed groups   as   per   grouping   on   Moodle.
Assessment criteria: See separate document
Submission components approximate breakdown (+/- 5%): 
Preliminary   Report                ~ 25%
Report to Client                               ~ 20%
Calculation   report                     ~ 45%
Code                                                                                  ~   10%
Formative    Submission    of Preliminary Report: Monday    2nd       December    (Hard      copy       including   drawings on one single A3 submitted to my   office   GM04   by   5pm)
QA Online Session early Jan (To be   agreed   closer to   submission)
Submission Date: 22th    Jan 2024   by 5pm.   No further extension   possible.   Not eligible   for   DAP Final Submission process: 
Submission   via    Moodle    using    the    submission    widget    in    the    GSA   Assignment    Tab    in    CEGE0009   Moodle   Page.   Upload one single zip folder per group. The folder should contain   four   separate   files:
1.      The    three    reports    in .pdf format             (you    must      resubmit    the      preliminary      report      and   drawings as   pdf)
2.       GSA   Model   (.gwb)
Please make sure the name of the zipfolder and all it contains includes your Group No.   Keep   the entire submission anonymous.
Background Figure   1   shows   the   plan   view   and   elevation   of   a   reinforced-concrete   frame,   which   is   the   structural   system supporting   an existing   building. The   building was originally   designed for   residential   use,   with   a   floor   imposed   load   of   1.5   kN/m2   .   This   full   imposed   load   was applied on the first two floor slabs,   whereas only half of this value acts   on the   top floor   slab   because   it   is just   a   roof. The   building   owner   is   now contemplating   changing the type   of occupancy   of the   building   from   residential   to   a   commercial   use.Figure 1. Diagrammatic structural Plan (top) and Elevation (Bottom) of a reinforced concrete frame.
Your job 
As   part   of   your   team,   you   are   working   as   structural   engineering   consultants   advising   the   client   on   whether the   proposed change of use   is structurally safe or   not.
Existing Frame Properties As   this    is   an   existing    reinforced    concrete   structure,   the    beams,   columns   and   slabs   already    have   cross-section   dimensions   and   reinforcement   detailing   as   provided   in   Figure   2   and   at   the   end   of   the   handout.   Your   task   is   to   assess   whether   the   existing   meets   the   relevant   code   checks   under   the   new   anticipated   design   loads   as   per   BS   EN   1992-1-1:2004.   The   allocated   structural   properties   (geometric   and    material)    as   well    as   the    new    imposed    load    category    can    be    found    on   the    last    page.    Shear   capacity   and   detailing   will   not   be   considered   but   a   shear   reinforcement   bar   diameter   is   provided   so   that   the   position   of the   bending   reinforcement   can   be   calculated.   The   assessment   of the   slabs   is   not   required.
GSA Modelling Using Oasys GSA 9,   you   will   build   a   wireframe   model   composed   of   1D   beam   elements   using   the   frame   dimensions   and   member   structural   properties   allocated   to   your   group   (see   Table   1).   As   per   usual   practice,   the   steel   reinforcement   is   not   included   in   FE   models;   however,   the   specific   weight   of reinforced concrete      should      be      used      so      that      gravity      loads      include      the      weight      of      the      steel   reinforcement. The ground-floor columns will be   modelled with a clamped   (fixed)   base.The floors   are   made   of two-way RC   slabs   spanning   between the   perimeter   beams   part   of the frame.   As you are   not   required to assess the slabs, they do   not   need to   be modelled explicitly (i.e.   using   2D   plate   elements)   but   their   load   (dead   +   live)   must   be   applied   on   the   skeletal   frame   using   either   1)   the   GSA   functionality   called   “area   grid   load”   (see   step-by-step   guide)   or   2)   Load   Panels.   Both   options   take   the   uniform   loads   applied   over   the   slab   area   and   distributes   them   automatically   on   the   adjacent   supporting       beams       using       the       tributary       area       method.       Since       the       loading       distribution       is       quite   straightforward,   both   grid   loading   and   load   panel   would   work.   The   dead   load   applied   on   all   slabs   includes   their   own   weight   +   a   super   imposed   load   of   1.2   kN/m2    for   floor   finishes.   Assume   all   slabs   have   a    150   mm   thickness   to   quantify   their   self-weight.   The   self-weight   of   the   remaining   structural   elements    (i.e.    columns    and    beams)    will    be    estimated    automatically    by    GSA    as    those      are    to      be   modelled explicitly as elements.Distributed   line   loads   of 3kN/m   should   be   also   applied   on   all the   perimeter   beams   supporting the first   and   second floors   only   in   order to   account for the weight   of   the   infill   walls   within   the   frame   (these   are   not   shown   in   Figure   1).   Regarding   the   live   load,   once   you   have   identified   the   appropriate   load   value   for your   building type,   apply that   on the first two floor slabs only.   The   roof   is   unchanged   so   use   the   original value   mentioned earlier (i.e. half   1.5kN/m2).Wind   load will   be   considered   acting   on   both   elevations. This   load will   be   applied   i代 写CEGE0009 Structural assessment of an existing building using GSA
代做程序编程语言n   GSA as   horizontal   point   loads on the   nodes of that façade   or   using   load   panels   using   a   pressure   load.   The   magnitude   of   each   point   load   will   be   calculated   by   hand   assuming   that   each   node   takes   the   resultant   of   the   wind   pressure   acting   on   its   tributary   area   of   the   façade   (same   method   as   column   tributary   area   under   gravity   loads   –   see   separate   handout   and   intro   presentation).   The wind   pressure   value   to   be   used   in   this calculation   is group-specific as provided   in Table   1.The   model   will   be   analysed   using   a   static,   linear   analysis.   In   order   to   identify   the   most   critical   design   internal   forces   that   each   member   will   experience,   the   following   load   combinations   (LCs)   should   be   defined and run (following   BS   EN   1990:2002 for   LC3-5):
1)       Permanent   Load
2)      Wind   Load
3)       1.35   Permanent   Load +   1.5   Imposed   Load
4)       1.35   Permanent   Load +   1.5 Wind   Load (including some consideration of   pattern   loading)
5)       1.35   Permanent   Load +   1.5   Imposed   Load + 0.75 Wind   Load
6)       1.35   Permanent   Load +   1.5   Imposed   Load + 0.75   Snow   LoadLoading   scenario   2   (Wind   only)   is   unrealistic   in   isolation   (since gravity   is   always   present)   and   unlikely   to   lead   to   critical   design   forces,   but   it   is   useful   for   the   purpose   of   appreciating   the   magnitude   and   shape   of the   internal   actions   (moment,   shear,   axial)   generated   by wind   loading   and to   make   it   easier   to check some results   by   hand   calculations.Load    patterning    means    turning    on    and      off    the      imposed      load    on      a      subset      of    floor      panels    while   permanent   loads   are   always   on.   This   is   not   codified   because   it’s   quite   project   specific   but   an   FE   model   allows   you   to   check   quite   a   few   combinations   fairly   quickly.   You   should   explore   this   for   one   floor   only   and   come   to   some judgement   about   whether   live   load   patterning   ever   makes   load   effects   worse and   if so where. This should feed into the   calcs   later.Although   the   deflected   shape   of   the    building   gives   some    useful    qualitative    information    and   often   allows   mistakes to   be spotted, quantitative   predictions of deflection from   this   type   of   simple   RC   model   require    a    lot    of    care.    A    basic    serviceability    assessment    can    still    be    carried    out      using    the    code.   References will be   provided for those who want to tackle this with the   FE model   as   a   bonus   challenge.
Deliverables per group: 
1.       Preliminary   Report
Drawings.
o   Plan + elevation +   perspective   on   one   single   A3
o   To scale
o   Indicate   load spanning directions
o   Assign a structural   grid
o   Indicate   levels   (SSL)
o   Draw actual cross-section sizes
o   Annotate as   necessary
Format:   1 single A3   print-out for formative submission and   pdf in final submission
Load estimation (wind,   load   patterning)
Format:   up to 2 pages, only your own   diagrams   allowed
Assessment   strategy   (What   can go wrong   if the   loads   are   increase?   How   are you   going to   check   this?   What   likely   failure   modes   which   will   drive   the   structural   assessment   drive   by   what   load combo?
Format:   up to   1 page, only your own diagrams   allowed
Embodied   CO2   Savings from   reuse   (i.e what would   be the   CO2   embodied   in the   structure   if it was   build   new). Format:   Up to   1 page, only your own   diagrams   allowed.
2.       Report   to the   clientThe   client   type   is   a   professional   building   manager.   They   are   not   structural   engineers   but   they   know   quite   a   lot   about   buildings   in   general.   They   won’t   care   about   modelling   details   but   will   be   able to   judge if a consultant   is acting   professionally and   competently or   not.
Brief   intro
Assessment   rationale   (no generic waffle about   FEM or stress/strain   or   RC   design   or   any   other   type   of waffle.   Building   managers   are   no-nonsense,   “bottom   line   people”   .   Put   yourself   in   their   shoes when you write your report.
Summary   table   comparing   calculated   member   capacities   and   critical   design   forces   obtained   from GSA (specify the load   case from which   it   comes from).
Conclude   with   your   final   professional   advice   to   the   client   and   some   suggestion   as   to   what   could   be done for the   proposed change of use to   be   possible.
Format:   up to 2 pages, up to two   GSA   graphs,   up to   two   tables.
3.       Calculation   Report – Should   include:
Resistance Assessment
Frame. stability assessment
Horizontal and vertical serviceability assessments
GSA   Model Validation Checks:
These are three   basic examples of checks that can   be   used to validate   this   GSA   model
o    Load      takedown:    floor      by      floor      hand      calculations      of      column      axial      forces      and      vertical   reactions due to dead load only +   comparison with   GSA vertical   reactions   at   column   base.
o    Identify   up   to   three   beams   (for   the   entire   frame)    most   likely   to   be   critically   loaded    under   gravity   only.   Justify   your   selection   with   simply   qualitative   considerations   of   loads,   spans   and   relevant   tributary   area.   Then   for   this   selection   calculate   by   hand   the   extreme   cases   for bending   moments and shears for the beams   in   x-direction   when   subjected   to   LC3   only.   Compare these with   relevant GSA output and comment on agreement/discrepancy.
o    Check    that      it’s      ok      to      model      the    frame      without      the      reinforcement      for      a      linear      elastic   analysis.    Calculate    the    uncracked      second    moment    for      the      beams      and      columns      (see   handout   on   Moodle)   and   replace   the   original   I   with   the   uncrack   I   and   compare   internal   forces   and   deflections   between   the   original   model   (with   gross   concrete   cross-section).   Comment.Format:   up   to   4   pages, no GSA graphs allowed,   only   your   own   diagrams   or   sketches   should   be   included   as   necessary   to   explain   calculations   and   results.   Hand-written   calculations   are fine   but   they   should   be clean, well explained and   illustrated.



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
