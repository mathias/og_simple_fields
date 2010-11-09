About:
======

This node, when enabled, forces Organic Group nodes to be Moderated (with no way to set it via the node edit form) and it also hides the Group Directory checkbox and Registration Form checkbox. We needed this module as a quick and dirty hack to simplify group nodes for nontechnical group moderators.

NOTE: This module doesn't have any settings. Once enabled and edited for your group node content type, it will simplify the form, but nothing else. No promises are made to its usefulness or compeleteness.
Use:
====

* Edit the og_simpl_fields.module file with the name of your content type in place of 'partnership'
* If more than one content type is a group type, add more switch cases like this:

  switch ($form_id) {
    // Replace 'partnership' with your content type below:
    case 'partnership_node_form':
    case 'other_group_node_form':
    case 'yet_another_group_node_edit_form':
    
* The cases will 'fall through' to all inherit the settings.
* To modify settings, use the following information:

  ['og_selective']['#default-value'] = # Set this to 
    0 for Open
    1 for Moderated
    2 for Invite Only
    3 for Closed

License:
========

This module is licensed under the [GNU General Public License](http://www.gnu.org/licenses/gpl.html).
