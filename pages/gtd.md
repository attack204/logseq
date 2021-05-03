---
title: GTD
---

## ## #.v-eisenhower-matrix
:PROPERTIES:
:template: v-eisenhower
:END:
### [[TODO]]
####
#+BEGIN_QUERY
{:query [:find (pull ?b [*])
         :where
         [?b :block/marker ?marker]
         (not (not [?b :block/ref-pages ?p]
         [?p :page/name ?page-name]
         [(clojure.string/includes? ?page-name "okr")])
         (not [?b :block/priority ?priority]
         [(contains? #{"A" "B" "C"} ?priority)]))
         [(contains? #{"DOING" "NOW"} ?marker)]]
 }
#+END_QUERY
####
####
####
### [[DECIDE]]
#### 
#+BEGIN_QUERY
{:query [:find (pull ?b [*])
         :where
         [?b :block/marker ?marker]
         (not (not [?b :block/ref-pages ?p]
         [?p :page/name ?page-name]
         [(clojure.string/includes? ?page-name "okr")])
         (not [?b :block/priority ?priority]
         [(contains? #{"A" "B" "C"} ?priority)]))
         [(contains? #{"TODO" "LATER"} ?marker)]]
 }
#+END_QUERY
####
### [[DELEGATE]]
####
####
####
### [[ELIMINATE]]
####
####
####
##
