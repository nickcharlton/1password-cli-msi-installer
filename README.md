# 1Password CLI MSI Installer

[1Password has a CLI tool][tool] that's very helpful for integrating into things
like setup scripts and handling development secrets more securely.

Unfortunately, on Windows, there's no installer. Instead, [you're prompted to
extract an archive, create the destination directory and add it to your
PATH][docs]. This is annoying once, impractical to do multiple times and enough
of a hurdle for others to be quite a pain, especially when you want to keep up
to date with the most recent version.

This project fills that gap and produces a (basic) MSI package for both x86 and
x64 using [their published releases][releases]. You can find them on the
[Releases page][msi-releases].

See also the companion blog post, which goes into more detail on how this works:
[_Building a 1Password CLI Windows MSI Installer_][blog-post].

## Building new releases

1. Fetch both new archives from 1Password's release site,
2. Update `Config.wxi` to the new version,
3. Build for both x86 and x64,
4. Commit the release (with the release notes) and tag,
5. Create a new release on GitHub, uploading the artifacts

[tool]: https://developer.1password.com/docs/cli/
[docs]: https://developer.1password.com/docs/cli/get-started#install
[releases]: https://app-updates.agilebits.com/product_history/CLI2
[msi-releases]: https://github.com/nickcharlton/1password-cli-msi-installer/releases
[blog-post]: https://nickcharlton.net/posts/building-a-1password-cli-windows-msi-installer
