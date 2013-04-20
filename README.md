# NAME

Graph::Algorithm::HITS - Anothor HITS algorithm implementation loading [Graph](http://search.cpan.org/perldoc?Graph)

# SYNOPSIS

    use Graph::Algorithm::HITS;
    use Graph;
    my $g = new Graph();
    $g->add_vertices(...);
    $g->add_edges(...);
    # Graph object as input
    my $hits = Graph::Algorithm::HITS(graph => $g);
    $hits->iterate(20); 
    # $auth_vector = { v1 => $auth_score_v1, v2 => $auth_score_v2,,, }
    my $auth_vector = $hits->get_authority();
    # $hub_vector = { $v1 => $hub_score_v1, v2 => $hub_score_v2,,, }
    my $hub_vector = $hits->get_hub();

# DESCRIPTION

Graph::Algorithm::HITS implements HITS algorithm (see [http://www2002.org/CDROM/refereed/643/node1.html](http://www2002.org/CDROM/refereed/643/node1.html)). There are a couple of HITS algorithm implementations in CPAN though, the reason you would choose this is that the score can be calculated by simply loading from [Graph](http://search.cpan.org/perldoc?Graph) object.

# AUTHOR

Shohei Kameda <shoheik@cpan.org>

# COPYRIGHT

Copyright 2013- Shohei Kameda

# LICENSE

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# SEE ALSO
