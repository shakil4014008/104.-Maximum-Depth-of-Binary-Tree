# 104.-Maximum-Depth-of-Binary-Tree

`````C#
class MaxDepthBinaryTree
    {     
        static void Main(string[] args)
        {
            TreeNode root = new TreeNode(1);
            root.left = new TreeNode(2);
            root.right = new TreeNode(3);
            root.left.left = new TreeNode(4);
            root.left.right = new TreeNode(5); 
            Console.WriteLine("Depth = " + MaxDepth(root));
            Console.ReadLine();
        }
        public static int MaxDepth(TreeNode root)
        {
            if (root == null) return 0;
            // find max of left and right and add 1
            return  1 + Math.Max(MaxDepth(root.left) , MaxDepth(root.right));
        }
    }
    
   public class TreeNode 
    {
       public int val;
       public TreeNode left;
       public TreeNode right;
       public TreeNode(int val=0, TreeNode left=null, TreeNode right=null) 
       {
          this.val = val;
          this.left = left;
          this.right = right;
       }
     } 
`````
