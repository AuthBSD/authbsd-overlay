* UNOFFICIAL KDE and XORG kit's @ MASTER BRANCHES *
( Gentoo-Staging with GLSA PATCHES )

- http://git.funtoo.org/gentoo-staging
- https://github.com/funtoo/merge-scripts

* Instructions:

Make sure that /etc/portage/repos.conf IS NOT a SYMLINK to /var/git/meta-repo/repos.conf

If it is, do: 

rm /etc/portage/repos.conf && mkdir /etc/portage/repos.conf 
ln -s /var/git/meta-repo/repos.conf /etc/portage/repos.conf/funtoo

cd /var/git/ && git clone https://github.com/AuthBSD/authbsd-overlay.git

Adding Kits ( you can use just THAT  you want )

Example for KDE-KIT :

cat << 'EOF' >> /etc/portage/repos.conf/kde-kit

[vmware]

location = /var/git/authbsd-overlay/kde-kit

auto-sync = no

priority = 10

EOF





