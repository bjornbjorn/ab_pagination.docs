Tags
====

AB Pagination will make a bunch of additional conditionals and variables available inside the {paginate} tag pair that resides inside the {exp:channel:entries} tag.

Variables
---------
On each page these variables are available:

* {abp_pages} - this is a tag pair loop with the links and in many cases the only thing you'll use. If so, skip to the description below.
* {abp_first_link} - the link to the first page
* {abp_last_link} - the link to the last page
* {abp_total_pages} - the total number of pages
* {abp_entry_from} - the start entry number on the current page
* {abp_entry_to} - the last entry number on the current page
* {abp_total_entries} - the total number of entries
* {abp_per_page} - the number of entries per page
* {abp_current_page_num} - the current page number, starting on 0 (zero-based indexing)
* {abp_current_page_num_liber} - the current page number, starting on 1
* {abp_previous_page_num} - the previous page number (zero-based indexing)
* {abp_previous_link} - the link to the previous page
* {abp_next_page_num} - the page number of the next page (zero-based indexing)
* {abp_next_link} - the link to the next page
* {abp_query_string} - contain the query strings, if any (for this to work config param enable_query_strings in EE must be set to TRUE)

Conditionals
------------
On each page these conditionals are available:

* {if abp_has_previous} - does this page have a previous page? (if not, we're on the first)
* {if abp_has_next} - does the current page have a next page? (if not, we're on the last)
* {if abp_last_page_not_linked} - true if the last page is not linked in the {abp_pages} loop (yes, this can actually come handy in some cases)

The {ab_pages} tag pair
-----------------------
The {abp_pages} tag pair has its own set of variables and conditionals, and since this is the most important tag it gets its own section here in the documentation.

{abp_pages} Parameters
----------------------
* padding - optional, defaults to 3. If you do not want padding, set this to "no"
* padding_left - optional, padding on the left side of the current page
* padding_right - optional, padding on the right side of the current page
* initial_size - optional, sets the initial number of pagelinks to show (by default the padding will decide this)
* fixed_size - optional, sets a fixed number of pagelinks to show (this will override all other settings, ie. padding and initial_size .. so just use like this: {abp_pages fixed_size="5"} )
* {abp_pages} Variables
* {abp_link} - the link to the page
* {abp_num} - the page number of the page (zero based)
* {abp_previous_link} - the link to the previous page (empty if none)
* {abp_previous_num} - the page number of the previous page (zero based)
* {abp_next_link} - the link to the next page (empty if none)
* {abp_next_num} - the page number of the next page (zero based)

{abp_pages} Conditionals
------------------------
* {if abp_is_current} - true if the current page in the loop is the current page
* {if abp_is_last_page} - true if the current page in the loop is the last page
* {if abp_is_first_page} - true if the current page in the loop is the first page
* {if abp_has_previous} - true if the current page in the loop has a previous page
* {if abp_has_next} - true if the current page in the loop has a next page