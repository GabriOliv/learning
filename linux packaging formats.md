# Summary: Libraries, Flatpak, and Snaps in Linux

- **Shared Libraries:**
  - Shared libraries in Linux reduce redundancy and save disk space.
  - These libraries are *tested and maintained* by the Linux distribution (distro) providers.

- **Dependency System:**
  - Linux applications rely on a *dependency system* for libraries.
  - However, this system has some drawbacks:
    - All packages need to use the *same version* of a library.
    - Older packages from older versions can potentially *break the library*.

- **Flatpak:**
  - *Flatpak* bundles everything an application needs to run.
  - It uses a runtime method and is compatible with almost any Linux distribution.
  - *Pros:* Simplifies application packaging and distribution.
  - *Cons:* Primarily suited for *graphical programs*; not suitable for installing system-wide libraries or command-line tools.

- **Snaps:**
  - *Snaps* follow a model similar to Flatpak, particularly in bundling applications and their dependencies.
  - Key differences include *automatic updates* and *containerization*.
  - Snaps run in a container with a separate file system, isolated from the host system.
  - They mount their file system as disks.
  - Snaps are commonly associated with *Ubuntu* but can be used on other distributions.
