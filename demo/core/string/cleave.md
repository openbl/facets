## String#cleave

    require 'facets/string/cleave'

no spaces short word

    s, x = 'whole', ['whole', '']
    s.cleave.assert == x

no spaces long word

    s, x = 'Supercalifragilisticexpialidocious' , ['Supercalifragilisticexpialidocious', '']
    s.cleave.assert == x

exact middle two words

    s, x = 'fancy split', ['fancy', 'split']
    s.cleave.assert == x

exact middle many words

    s, x = 'All good Rubyists know how to party', ['All good Rubyists', 'know how to party']
    s.cleave.assert == x

closer to start

    s, x = 'short splitter', ['short', 'splitter']
    s.cleave.assert == x

closer to start

    s, x = 'Four score and seven years ago...', ['Four score and', 'seven years ago...']
    s.cleave.assert == x

closer to start

    s, x = 'abc def ghijklm nop', ['abc def', 'ghijklm nop']
    s.cleave.assert == x

closer to end

    s, x = 'extended split', ['extended', 'split']
    s.cleave.assert == x

closer to end

    s, x = 'abc defghi jklm nop', [ 'abc defghi', 'jklm nop']
    s.cleave.assert == x

