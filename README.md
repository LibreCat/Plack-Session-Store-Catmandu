# NAME

Plack::Session::Store::Catmandu - Plack session store backed by a Catmandu::Store

# VERSION

Version 0.02

# SYNOPSIS

    use Plack::Builder;
    use Plack::Middleware::Session;
    use Plack::Session::Store::Catmandu;

    my $app = sub {
        return [ 200, [ 'Content-Type' => 'text/plain' ], [ 'Hello' ] ];
    };

    builder {
        enable 'Session', store => Plack::Session::Store::Catmandu->new(
            store => 'MongoDB',
            bag => 'sessions',
        );
        $app;
    };

# SEE ALSO

[Plack::Middleware::Session](https://metacpan.org/pod/Plack::Middleware::Session), [Catmandu](https://metacpan.org/pod/Catmandu)

# AUTHOR

Nicolas Steenlant, `<nicolas.steenlant at ugent.be>`

# LICENSE AND COPYRIGHT

This program is free software; you can redistribute it and/or modify it
under the terms of either: the GNU General Public License as published
by the Free Software Foundation; or the Artistic License.

See http://dev.perl.org/licenses/ for more information.
