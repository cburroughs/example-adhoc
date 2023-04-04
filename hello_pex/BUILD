python_source(
    name='lib-hello',
    source='hello.py')

pex_binary(
    name="hi",
    entry_point="hello.py",
)

adhoc_tool(
    name="local-data",
    runnable=":hi",
    args=["--foo"],
    output_directories=["data"],
    log_output=True,
)

python_source(
    name='lib-world',
    source='world.py',
    dependencies=[':local-data']
)



