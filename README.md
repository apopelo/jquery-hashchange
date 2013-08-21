jQuery Hashchange [![Build Status](https://travis-ci.org/apopelo/jquery-hashchange.png)](https://travis-ci.org/apopelo/jquery-hashchange)
=================

Simple and lightweight plugin which allows to bind callbacks to specific
`window.location.hash` values.

Example:

    /*

    Code below means:

        1. Call onSet() callback each time when url changes to
           http://.../#!/login/

        2. Call onRemove() callback each time when url changes from
           http://.../#!/login/ to anything else, e.g.
           http://.../#!/ or http://.../

    */
    $(window).hashchange({
        hash: "#!/login/",
        onSet: function() {
            $("#login-form").show();
        },
        onRemove: function() {
            $("#login-form").hide();
        },
    });
