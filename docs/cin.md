# cin
`cin` (named after C++'s cin function), allows you to easily take user input through the console.

## Basic Usage
`cin` is defined in Cerbose as:
```python
def cin(type, tag, text, options, *, log=False, logfile=None, logfeedback=False, textcol="normal", stagtype=None, timestamp=False, lower=False, showop=True):
```
This means that `type`, `text`, and `options` are required inputs, and the rest are optional keyword arguments.  
You may notice that the keyword arguments and even some of the required inputs are suspiciously similar to those of `cprint`. This is because `cin` uses an `mprint` call to display its prompts.  
Here is an example call:
```python
res = cin('ok', 'Hello,\nworld!', 'any')
print(res)
```
Output (again...assuming default configuration...)
```plaintext
[OK]: Hello,
    : world!:
> answer  # this answer is not automatic output, assume this is the answer the user typed in
answer  # this is the print(res) activating.
```
There are a lot of things you can observe from this.
**NOTE**: `cin` returns the answer you get from it, and also makes this interactive prompt.  

The prompt ("Hello,\nworld!") uses the exact same keyword arguments as `cprint`. The `type` and `text`
