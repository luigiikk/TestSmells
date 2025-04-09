## The Operating System Evangelist


```python
class LutrisWrapperTestCase(unittest.TestCase):
    def test_excluded_initial_process(self):
        "Test that an excluded process that starts a monitored process works"
        env = os.environ.copy()
        env['PYTHONPATH'] = ':'.join(sys.path)
        # run the lutris-wrapper with a bash subshell. bash is "excluded"
        wrapper_proc = subprocess.Popen(
            [
                sys.executable, lutris_wrapper_bin, 'title', '0', '1', 'bash', 'bash',
                '-c',
                "echo Hello World; exec 1>&-; while sleep infinity; do true; done"
            ],
            stdin=subprocess.DEVNULL, stdout=subprocess.PIPE, env=env,
        )