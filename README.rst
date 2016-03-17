Flexidate Python3::

Python 3 port of Flexidate
Date parsing and normalization utilities based on FlexiDate.

To parse dates use parse, e.g.::

    from flexidate import parse
    parse('1890') -> FlexiDate(year=u'1890')
    parse('1890?') -> FlexiDate(year=u'1890', qualifier='Uncertainty: 1890?')

Once you have a FlexiDate you can get access to attributes (strings of course
...)::

    from flexidate import parse
    fd = parse('Jan 1890')
    fd.year # u'1890'
    fd.month # u'01'

Note how all fields are retained as strings -- this is the only way to not lose
information.

However, it's easy to convert to other forms::

    fd.as_float() # 1890
    fd.as_datetime() # datetime(1890,01,01)



