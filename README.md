# TWIG-DEBUG
Modification activates the built-in debug function in TWIG.

! [TWIG-DEBUG] (twig_dump.png)

## Description
The dump feature displays information about the template variable. 
This is mainly useful for debugging a template that does not behave properly, analyzing its variables:
`` `twig
{{dump (user)}}
`` ``

In the context of HTML wrap the output by a preliminary tag to read it easier to read:
`` `twig
<Pre >.
    {{dump (user)}}
</ pre>
`` ``

> Using a pre-tag is not required if Xdebug is enabled and the HTML_ERRORS 
> is enabled; As a bonus, the output is also better with Xdebug included.

You can debug a few variables by passing them as additional arguments:
`` `twig
{{DUMP (User, Categories)}}
`` ``

If you do not give any value, all variables from the current context will be reset:
`` `twig
{{dump ()}}
`` ``
Internally, TWIG uses the PHP VAR_DUMP function.

### compatibility
- OpenCart 3.0.3.x.

## Links
- [Forum resource] (https://forum.opencart.name/resources/54/)
- [DUMP - Documentation - TWIG] (https://twig.symfony.com/doc/3.x/functions/dump.html)
