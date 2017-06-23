# Regexes
Regex Examples

  [https://sourceforge.net/p/notepad-plus/discussion/331754/thread/37889029/]
  [http://boost.sourceforge.net/libs/regex/doc/syntax_basic.html]
  [http://www.boost.org/doc/libs/1_48_0/libs/regex/doc/html/boost_regex/format/boost_format_syntax.html]
  [http://zett42.de/software/boost-regex-playground/]


`(?<Dim>Dim)(\s)(?<ObjectName>\w+)(\s)(As )(?<ObjectType>\w+)`

`$+{ObjectType} $+{ObjectName};`

2 or less argument sub

`(?<AccessModifier>Public|Private|Friend)(\s)(Sub)(\s+)(?<MethodName>\w+)(\()(?<ParamPass1>ByRef|ByVal)*(\s)*(?<ParamName1>\w+)*(\s)*(As)*(\s)*(?<ParamType1>\w+)*(?<ParamSeparator1>,)*(\s)*(?<ParamPass2>ByRef|ByVal)*(\s)*(?<ParamName2>\w+)*(\s)*(As)*(\s)*(?<ParamType2>\w+)*(\))(\s)*(As)*(\s)*(?<ReturnType>\w+)`
`\L$+{AccessModifier} void \E$+{MethodName}\($+{ParamPass1} $+{ParamType1} $+{ParamName1}$+{ParamSeparator1}$+{ParamPass2} $+{ParamType2} $+{ParamName2})\r{`

2 or less argument function

`(?<AccessModifier>Public|Private|Friend)(\s)(Function)(\s+)(?<MethodName>\w+)(\()(?<ParamPass1>ByRef|ByVal)*(\s)*(?<ParamName1>\w+)*(\s)*(As)*(\s)*(?<ParamType1>\w+)*(?<ParamSeparator1>,)*(\s)*(?<ParamPass2>ByRef|ByVal)*(\s)*(?<ParamName2>\w+)*(\s)*(As)*(\s)*(?<ParamType2>\w+)*(\))(\s)*(As)*(\s)*(?<ReturnType>\w+)`

`\L$+{AccessModifier} \E$+{ReturnType} $+{MethodName}\($+{ParamPass1} $+{ParamType1} $+{ParamName1}$+{ParamSeparator1}$+{ParamPass2} $+{ParamType2} $+{ParamName2})\r{`

