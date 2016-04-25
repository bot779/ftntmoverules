# ftntmoverules
Generate CLI commands to move groups of Fortigate Firewall Policy rules

Have you ever tried importing firewall rules into a fortigate firewall?
You can use "edit 0" to append rules to the end of the Firewall Policy.
That sounds like a safe way to do things (the new rules will fall after your "deny all" rule and have no effect)

When it comes time to move a new section of rules to a location where they can take effect you'll find:
There's no convenient way to move a group of rules.
You can move one rule at a time but not a set of rules.

This command (ftntmoverules) generates a set of "move" commands to move a number of commands from one spot in the firewall policy to another.

Usage:
./ftntmoverules [OPTIONS]
OPTIONS:
--help -? -h
--from <rulenum> ;# the first rule number of the set of rules to be moved
--before <rulenum> ;# insert rules before this rule number
--count <numberofrules> ;# the number of rules to be moved
