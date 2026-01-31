![](./images/image001.png)

![](./images/image002.png)

![](./images/image003.png)

The current set, here wxwidgets_3_3, is defined by cloning the default one, then modifying it. Don't forget to save the result!

cb_build **base** is defines used to ed but not used here in \*\_windows.cbp versions. You can leave it empty (to set an empty string, **or set it with ""**, just because it is written that "the base number is mandatory". But it's not a problem here). You can also define it with the full path to codeblocks/src, for me it's:

D:\\Users\\Gerard\\Documents\\CodeBlocks_SVN\\CodeBlocks_src\\src. It may be used for plugins where the full path is needed.

cb_build **cflags** **must be defined**. Here, it is -O2. You can also define it with -g to obtain a C::B debug version. If you don't want to set it, don't set it to an empty field, but define it as "".

cb_build **cpp_std** is used to set a compilation option as -std=… It's equivalent to the standard variable cb_cpp_std but without the string -std=. Note that \_windows.cbp only use cb.build.cpp_std, so they may be different.

To be compatible with standard cbp versions (as \*wx32_64.cbp), use cpp_std with gnu++11 as value (instead of gnu++20).

cb_build **osbits** is used to set the number of bits of the OS: 32 or 64 bits

cb_release_type is defined for wx31_64 cbps (and other wxWidgets versions), **but not used with \_windows versions** and is equivalent to cb_build.cflags As \*\_windows.cbp only use cb.build.cflags: they may be different.

As configured here, it is compatible with standard versions, Andrew Cottrell's old/new versions and mine.

wxwidgets variable contains 3 user-defined fields:

- wx_cfg, here contains an empty string for a standard wxWidgets version. **Don't leave it as blank, but set it to ""**. It could be a single letter d for a debug wxWidgets version;
- wx_suffix normally contains the letter u, for Unicode;
- wx_version reflect the wxwidgets version, here 33 for all versions 3.3. (3.3.0, 3.3.1, …)

_Note_: They correspond to environment variables in standard cbp files:

&lt;Environment&gt;

    &lt;Variable name="WX_CFG" value="" /&gt;

    &lt;Variable name="WX_SUFFIX" value="u" /&gt;

    &lt;Variable name="WX_VERSION" value="33" /&gt;

&lt;/Environment&gt;

**How to use them**:

Load in a usable Code::Blocks executable (for example an official version or a nightly) the workspace CodeBlocks_Windows.workspace. It contains all links to the \*\_Windows.cbp. If necessary, C::B will ask you to set some global variables if they have not been set previously.

**Make a full generation the first time you use it**.

At the end, use the updateWindows.bat file to create a working stripped version in the corresponding outputxx_yy. xx is equal to wx_version and yy to osbits. With parameters given in previous images, it will be output33_64.

**updateWindows.bat is always created by Codeblocks_Windows.cbp**.

Note that if you create a version for other wxWidgets versions, you'll have simply to modify the global variables.